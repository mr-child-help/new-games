---
title: Adding a workflow status badge
intro: You can display a status badge in your repository to indicate the status of your workflows.
redirect_from:
  - /actions/managing-workflow-runs/adding-a-workflow-status-badge
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
shortTitle: Add a status badge
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

{% data reusables.repositories.actions-workflow-status-badge-intro %}

You reference the workflow by the name of your workflow file.

```markdown
![example workflow]({% ifversion fpt or ghec %}https://github.com{% else %}<HOSTNAME>{% endif %}/<OWNER>/<REPOSITORY>/actions/workflows/<WORKFLOW_FILE>/badge.svg)
```
## Using the workflow file name

In diesem Markdown-Beispiel wird ein Status-Badge für einen Workflow mit dem Dateipfad `.github/workflows/main.yml`hinzugefügt. The `OWNER` of the repository is the `github` organization and the `REPOSITORY` name is `docs`.

```markdown
![example workflow](https://github.com/github/docs/actions/workflows/main.yml/badge.svg)
```

## Using the `branch` parameter

In diesem Markdown-Beispiel wird ein Status-Badge für eine Verzweigung mit dem Namen `Feature-1-`hinzugefügt.

```markdown
![example branch parameter](https://github.com/github/docs/actions/workflows/main.yml/badge.svg?branch=feature-1)
```

## Using the `event` parameter

In diesem Markdown-Beispiel wird ein Badge hinzugefügt, das den Status von Workflowausführungen anzeigt, die durch das `pull_request` -Ereignis ausgelöst werden.

```markdown
![example event parameter](https://github.com/github/docs/actions/workflows/main.yml/badge.svg?event=pull_request)
```
