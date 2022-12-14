---
title: Issue in ein anderes Repository übertragen
intro: 'Wenn Du einen offenen Issue in ein anderes, geeigneteres Repository verschieben möchtest, kannst Du ihn in das gewünschte Repository übertragen.'
redirect_from:
  - /github/managing-your-work-on-github/managing-your-work-with-issues-and-pull-requests/transferring-an-issue-to-another-repository
  - /articles/transferring-an-issue-to-another-repository
  - /github/managing-your-work-on-github/transferring-an-issue-to-another-repository
  - /issues/tracking-your-work-with-issues/managing-issues/transferring-an-issue-to-another-repository
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Transfer an issue
---

To transfer an open issue to another repository, you must have write access to the repository the issue is in and the repository you're transferring the issue to. For more information, see "[Repository roles for an organization](/organizations/managing-access-to-your-organizations-repositories/repository-roles-for-an-organization)."

Du kannst Issues nur zwischen Repositorys übertragen, die demselben Benutzer- oder Organisationskonto angehören. {% ifversion fpt or ghes or ghec %}You can't transfer an issue from a private repository to a public repository.{% endif %}

Wenn Du einen Issue überträgst, bleiben seine Kommentare und Bearbeiter erhalten. The issue's labels and milestones are not retained. This issue will stay on any user-owned or organization-wide project boards and be removed from any repository project boards. Weitere Informationen findest Du unter „[Informationen zu Projektboards](/articles/about-project-boards).“

Im Issue erwähnte Personen und Teams werden über die Übertragung des Issues in ein neues Repository benachrichtigt. Die ursprüngliche URL wird an die neue URL des Issues weitergeleitet. Personen, die für das neue Repository über keine Leseberechtigung verfügen, wird ein Banner angezeigt, das sie darüber informiert, dass der Issue in ein Repository übertragen wurde, auf das sie keinen Zugriff haben.

## Offener Issue in ein anderes Repository übertragen

{% include tool-switcher %}

{% webui %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-issues %}
3. Klicke in der Liste der Issues auf den Issue, den Du übertragen möchtest.
4. Klicke in der rechten Seitenleiste auf **Transfer issue** (Issue übertragen). ![Schaltfläche zum Übertragen eines Issues](/assets/images/help/repository/transfer-issue.png)
5. Wähle im Dropdownmenü **Choose a repository** (Repository auswählen) das Repository aus, in das Du den Issue übertragen möchtest. ![Auswahl eines Repositorys](/assets/images/help/repository/choose-a-repository.png)
6. Klicke auf **Transfer issue** (Issue übertragen). ![Schaltfläche „Transfer issue“ (Issue übertragen)](/assets/images/help/repository/transfer-issue-button.png)

{% endwebui %}

{% cli %}

{% data reusables.cli.cli-learn-more %}

To transfer an issue, use the `gh issue transfer` subcommand. Replace the `issue` parameter with the number or URL of the issue. Replace the `{% ifversion ghes %}hostname/{% endif %}owner/repo` parameter with the {% ifversion ghes %}URL{% else %}name{% endif %} of the repository that you want to transfer the issue to, such as `{% ifversion ghes %}https://ghe.io/{% endif %}octocat/octo-repo`.

```shell
gh issue transfer <em>issue</em> <em>{% ifversion ghes %}hostname/{% endif %}owner/repo</em>
```

{% endcli %}

## Weiterführende Informationen

- „[Informationen zu Issues](/articles/about-issues)“
- „[Sicherheitsprotokoll überprüfen](/articles/reviewing-your-security-log)“
- „[Auditprotokoll Deiner Organisation überprüfen](/organizations/keeping-your-organization-secure/reviewing-the-audit-log-for-your-organization)“
