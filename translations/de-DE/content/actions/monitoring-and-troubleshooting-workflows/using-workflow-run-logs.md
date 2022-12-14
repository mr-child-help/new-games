---
title: Using workflow run logs
intro: 'You can view, search, and download the logs for each job in a workflow run.'
redirect_from:
  - /actions/managing-workflow-runs/using-workflow-run-logs
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

Auf der Workflow-Lauf-Seite können sie sehen, ob ein Workflow-Lauf ausgeführt wird oder abgeschlossen ist. Sie müssen mit einem {% data variables.product.prodname_dotcom %}-Konto angemeldet sein, um Workflow-Informationen anzuzeigen, auch für öffentliche Repositories. Weitere Informationen finden Sie unter „[Zugriffsberechtigungen auf GitHub](/articles/access-permissions-on-github)“.

Wenn der Lauf abgeschlossen ist, können Sie sehen, ob das Ergebnis erfolgreich, fehlerhaft, abgebrochen oder neutral war. Wenn der Lauf fehlgeschlagen ist, können Sie die Build-Protokolle anzeigen und durchsuchen, um den Fehler zu diagnostizieren und den Workflow erneut auszuführen. Sie können auch fakturierbare Auftragsausführungsminuten anzeigen oder Protokolle herunterladen und Artefakte erstellen.

{% data variables.product.prodname_actions %} verwenden die Checks API, um Status, Ergebnisse und Protokolle für einen Workflow auszugeben. {% data variables.product.prodname_dotcom %} erstellt eine neue Prüfsuite für jeden Workflow-Lauf. Die Prüfsuite enthält einen Prüflauf für jeden Auftrag im Workflow, und jeder Auftrag enthält Schritte. {% data variables.product.prodname_actions %} werden als Schritt in einem Workflow ausgeführt. For more information about the Checks API, see "[Checks](/rest/reference/checks)."

{% data reusables.github-actions.invalid-workflow-files %}

## Protokolle zur Fehlerdiagnose anzeigen

Wenn Ihr Workflow-Lauf fehlschlägt, können Sie sehen, welcher Schritt den Fehler verursacht hat, und die Build-Protokolle des fehlgeschlagenen Schrittes zur Fehlerbehebung überprüfen. Sie sehen, wie lange es gedauert hat, bis jeder Schritt ausgeführt wurde. Sie können außerdem einen Permalink in eine bestimmte Zeile in der Protokolldatei kopieren, um ihn mit Ihrem Team zu teilen. {% data reusables.repositories.permissions-statement-read %}

In addition to the steps configured in the workflow file, {% data variables.product.prodname_dotcom %} adds two additional steps to each job to set up and complete the job's execution. These steps are logged in the workflow run with the names "Set up job" and "Complete job".

For jobs run on {% data variables.product.prodname_dotcom %}-hosted runners, "Set up job" records details of the runner's virtual environment, and includes a link to the list of preinstalled tools that were present on the runner machine.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.actions-tab %}
{% data reusables.repositories.navigate-to-workflow-superlinter %}
{% data reusables.repositories.view-run-superlinter %}
{% data reusables.repositories.navigate-to-job-superlinter %}
{% data reusables.repositories.view-failed-job-results-superlinter %}
{% data reusables.repositories.view-specific-line-superlinter %}

## Protokolle durchsuchen

Sie können die Build-Protokolle für einen bestimmten Schritt durchsuchen. Beim Durchsuchen von Protokollen werden nur eingeblendete Schritte in die Ergebnisse einbezogen. {% data reusables.repositories.permissions-statement-read %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.actions-tab %}
{% data reusables.repositories.navigate-to-workflow-superlinter %}
{% data reusables.repositories.view-run-superlinter %}
{% data reusables.repositories.navigate-to-job-superlinter %}
1. Gib in der oberen rechten Ecke der Protokollausgabe im Suchfeld **Search logs** (Protokolle durchsuchen) eine Suchanfrage ein.
{% ifversion fpt or ghes > 3.0 or ghae or ghec %}
  ![Suchfeld zum Durchsuchen von Protokollen](/assets/images/help/repository/search-log-box-updated-2.png)
{% else %}
  ![Suchfeld zum Durchsuchen von Protokollen](/assets/images/help/repository/search-log-box-updated.png)
{% endif %}

## Herunterladen von Protokollen

Sie können die Protokolldateien von Ihrem Workflowlauf herunterladen. Sie können auch die Artefakte eines Workflows herunterladen. Weitere Informationen findest Du unter „[Workflow-Daten mittels Artefakten persistieren](/actions/automating-your-workflow-with-github-actions/persisting-workflow-data-using-artifacts)“. {% data reusables.repositories.permissions-statement-read %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.actions-tab %}
{% data reusables.repositories.navigate-to-workflow-superlinter %}
{% data reusables.repositories.view-run-superlinter %}
{% data reusables.repositories.navigate-to-job-superlinter %}
1. In the upper right corner, click {% ifversion fpt or ghes > 3.0 or ghae or ghec %}{% octicon "gear" aria-label="The gear icon" %}{% else %}{% octicon "kebab-horizontal" aria-label="The horizontal kebab icon" %}{% endif %} and select **Download log archive**.
  {% ifversion fpt or ghes > 3.0 or ghae or ghec %}
  ![Dropdownmenü zum Herunterladen von Protokollen](/assets/images/help/repository/download-logs-drop-down-updated-2.png)
  {% else %}
  ![Dropdownmenü zum Herunterladen von Protokollen](/assets/images/help/repository/download-logs-drop-down-updated.png)
  {% endif %}

## Logs löschen

Du kannst die Logdateien aus Deiner Workflow-Ausführung löschen. {% data reusables.repositories.permissions-statement-write %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.actions-tab %}
{% data reusables.repositories.navigate-to-workflow-superlinter %}
{% data reusables.repositories.view-run-superlinter %}
1. In the upper right corner, click {% octicon "kebab-horizontal" aria-label="The horizontal kebab icon" %}.
    {% ifversion fpt or ghes > 3.0 or ghae or ghec %}
    ![Kebab-horizontal icon](/assets/images/help/repository/workflow-run-kebab-horizontal-icon-updated-2.png)
    {% else %}
    ![Kebab-horizontal icon](/assets/images/help/repository/workflow-run-kebab-horizontal-icon-updated.png)
    {% endif %}
2. Um die Logdateien zu löschen, klicke auf **Delete all logs** (Alle Logs löschen) und überprüfe die Bestätigungsanfrage.
  {% ifversion fpt or ghes > 3.0 or ghae or ghec %}
  ![Delete all logs](/assets/images/help/repository/delete-all-logs-updated-2.png)
  {% else %}
  ![Delete all logs](/assets/images/help/repository/delete-all-logs-updated.png)
  {% endif %}
After deleting logs, the **Delete all logs** button is removed to indicate that no log files remain in the workflow run.

## Viewing logs with {% data variables.product.prodname_cli %}

{% data reusables.cli.cli-learn-more %}

To view the log for a specific job, use the `run view` subcommand. Replace `run-id` with the ID of run that you want to view logs for. {% data variables.product.prodname_cli %} returns an interactive menu for you to choose a job from the run. If you don't specify `run-id`, {% data variables.product.prodname_cli %} returns an interactive menu for you to choose a recent run, and then returns another interactive menu for you to choose a job from the run.

```shell
gh run view <em>run-id</em> --log
```

You can also use the `--job` flag to specify a job ID. Replace `job-id` with the ID of the job that you want to view logs for.

```shell
gh run view --job <em>job-id</em> --log
```

You can use `grep` to search the log. For example, this command will return all log entries that contain the word `error`.

```shell
gh run view --job <em>job-id</em> --log | grep error
```

To filter the logs for any failed steps, use `--log-failed` instead of `--log`.

```shell
gh run view --job <em>job-id</em> --log-failed
```
