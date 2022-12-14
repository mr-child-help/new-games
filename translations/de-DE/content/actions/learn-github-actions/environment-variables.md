---
title: Umgebungsvariablen
intro: '{% data variables.product.prodname_dotcom %} setzt Standard-Umgebungsvariablen für jeden {% data variables.product.prodname_actions %}-Workflow-Lauf. Du kannst auch benutzerdefinierte Umgebungsvariablen in Deiner Workflow-Datei festlegen.'
redirect_from:
  - /github/automating-your-workflow-with-github-actions/using-environment-variables
  - /actions/automating-your-workflow-with-github-actions/using-environment-variables
  - /actions/configuring-and-managing-workflows/using-environment-variables
  - /actions/reference/environment-variables
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

## Informationen zu Umgebungsvariablen

{% data variables.product.prodname_dotcom %} setzt Standard-Umgebungsvariablen, die für jeden Schritt in einem Workflow-Lauf verfügbar sind. Bei Umgebungsvariablen wird die Groß-/Kleinschreibung berücksichtigt. Befehle, die in Aktionen oder „Steps“ (Schritten) ausgeführt werden, können Umgebungsvariablen erstellen, lesen und ändern.

Um benutzerdefinierte Umgebungsvariablen festzulegen, musst Du die Variablen in der Workflow-Datei angeben. You can define environment variables for a step, job, or entire workflow using the [`jobs.<job_id>.steps[*].env`](/github/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions#jobsjob_idstepsenv), [`jobs.<job_id>.env`](/github/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions#jobsjob_idenv), and [`env`](/github/automating-your-workflow-with-github-actions/workflow-syntax-for-github-actions#env) keywords. Weitere Informationen finden Sie unter „[Workflow-Syntax für {% data variables.product.prodname_dotcom %}](/articles/workflow-syntax-for-github-actions/#jobsjob_idstepsenv)“.

{% raw %}
```yaml
jobs:
  weekday_job:
    runs-on: ubuntu-latest
    env:
      DAY_OF_WEEK: Mon
    steps:
      - name: "Hello world when it's Monday"
        if: ${{ env.DAY_OF_WEEK == 'Mon' }}
        run: echo "Hello $FIRST_NAME $middle_name $Last_Name, today is Monday!"
        env:
          FIRST_NAME: Mona
          middle_name: The
          Last_Name: Octocat
```
{% endraw %}

To use the value of an environment variable in a workflow file, you should use the [`env` context](/actions/reference/context-and-expression-syntax-for-github-actions#env-context). If you want to use the value of an environment variable inside a runner, you can use the runner operating system's normal method for reading environment variables.

If you use the workflow file's `run` key to read environment variables from within the runner operating system (as shown in the example above), the variable is substituted in the runner operating system after the job is sent to the runner. For other parts of a workflow file, you must use the `env` context to read environment variables; this is because workflow keys (such as `if`) require the variable to be substituted during workflow processing before it is sent to the runner.

You can also use the `GITHUB_ENV` environment file to set an environment variable that the following steps in a job can use. The environment file can be used directly by an action or as a shell command in a workflow file using the `run` keyword. Weitere Informationen findest Du unter „[Workflow-Befehle für {% data variables.product.prodname_actions %}](/actions/reference/workflow-commands-for-github-actions/#setting-an-environment-variable)“.

## Standard-Umgebungsvariablen

Es wird dringend empfohlen, dass Aktionen Umgebungsvariablen verwenden, um auf das Dateisystem zuzugreifen, anstatt hartcodierte Dateipfade zu verwenden. {% data variables.product.prodname_dotcom %} legt Umgebungsvariablen für Aktionen fest, die in allen Runner-Umgebungen verwendet werden sollen.

| Umgebungsvariable    | Beschreibung                                                                                                                                                                                                                                                                                               |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `CI`                 | Immer auf `true` gesetzt.                                                                                                                                                                                                                                                                                  |
| `GITHUB_WORKFLOW`    | Der Name des Workflows.                                                                                                                                                                                                                                                                                    |
| `GITHUB_RUN_ID`      | {% data reusables.github-actions.run_id_description %}
| `GITHUB_RUN_NUMBER`  | {% data reusables.github-actions.run_number_description %}
| `GITHUB_JOB`         | The [job_id](/actions/reference/workflow-syntax-for-github-actions#jobsjob_id) of the current job.                                                                                                                                                                                                         |
| `GITHUB_ACTION`      | Die eindeutige Kennung (`id`) der Aktion.                                                                                                                                                                                                                                                                  |
| `GITHUB_ACTION_PATH` | The path where your action is located. You can use this path to access files located in the same repository as your action. This variable is only supported in composite actions.                                                                                                                          |
| `GITHUB_ACTIONS`     | Immer auf `true` gesetzt, wenn {% data variables.product.prodname_actions %} den Workflow ausführt. Du kannst diese Variable verwenden, um zu differenzieren, wann Tests lokal oder von {% data variables.product.prodname_actions %} durchgeführt werden.                                               |
| `GITHUB_ACTOR`       | Name der Person oder App, die den Workflow initiiert hat. Beispiel: `octocat`.                                                                                                                                                                                                                             |
| `GITHUB_REPOSITORY`  | Der Inhaber- und Repository-Name, Beispiel: `octocat/Hello-World`.                                                                                                                                                                                                                                         |
| `GITHUB_EVENT_NAME`  | Name des Webhook-Ereignisses, das den Workflow ausgelöst hat.                                                                                                                                                                                                                                              |
| `GITHUB_EVENT_PATH`  | Pfad der Datei mit der gesamten Nutzlast des Webhook-Ereignisses. Beispiel: `/github/workflow/event.json`.                                                                                                                                                                                                 |
| `GITHUB_WORKSPACE`   | The {% data variables.product.prodname_dotcom %} workspace directory path, initially empty. Beispiel: `/home/runner/work/my-repo-name/my-repo-name`. The [actions/checkout](https://github.com/actions/checkout) action will check out files, by default a copy of your repository, within this directory. |
| `GITHUB_SHA`         | Commit-SHA, die den Workflow ausgelöst hat. Beispiel: `ffac537e6cbbf934b08745a378932722df287a53`.                                                                                                                                                                                                          |
| `GITHUB_REF`         | Branch- oder Tag-Ref, das den Workflow ausgelöst hat. Beispiel: `refs/heads/feature-branch-1`. Wenn für den Ereignistyp weder ein Branch noch ein Tag vorliegt, ist die Variable nicht vorhanden.                                                                                                          |
| `GITHUB_HEAD_REF`    | Only set for pull request events. The name of the head branch.                                                                                                                                                                                                                                             |
| `GITHUB_BASE_REF`    | Only set for pull request events. The name of the base branch.                                                                                                                                                                                                                                             |
| `GITHUB_SERVER_URL`  | Returns the URL of the {% data variables.product.product_name %} server. For example: `https://{% data variables.product.product_url %}`.                                                                                                                                                                  |
| `GITHUB_API_URL`     | Gibt die API-URL zurück. For example: `{% data variables.product.api_url_code %}`.                                                                                                                                                                                                                         |
| `GITHUB_GRAPHQL_URL` | Gibt die GraphQL-API-URL zurück. For example: `{% data variables.product.graphql_url_code %}`.                                                                                                                                                                                                             |
| `RUNNER_NAME`        | {% data reusables.actions.runner-name-description %}
| `RUNNER_OS`          | {% data reusables.actions.runner-os-description %}
| `RUNNER_TEMP`        | {% data reusables.actions.runner-temp-directory-description %}
{% ifversion not ghae %}| `RUNNER_TOOL_CACHE` | {% data reusables.actions.runner-tool-cache-description %}{% endif %}

{% tip %}

**Note:** If you need to use a workflow run's URL from within a job, you can combine these environment variables: `$GITHUB_SERVER_URL/$GITHUB_REPOSITORY/actions/runs/$GITHUB_RUN_ID`

{% endtip %}

### Determining when to use default environment variables or contexts

{% data reusables.github-actions.using-context-or-environment-variables %}

## Namens-Konventionen für Umgebungsvariablen

When you set a custom environment variable, you cannot use any of the default environment variable names listed above with the prefix `GITHUB_`. If you attempt to override the value of one of these default environment variables, the assignment is ignored.

Alle neuen Umgebungsvariablen, die auf einen Speicherort im Dateisystem verweisen, müssen das Suffix `_PATH` erhalten. Die Standardvariablen `HOME` und `GITHUB_WORKSPACE` sind von dieser Konvention ausgenommen, da die Bezeichnungen „home“ und „workspace“ bereits einen Speicherort implizieren.
