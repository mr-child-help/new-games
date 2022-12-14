---
title: Ein Repository klonen
intro: 'When you create a repository on {% data variables.product.product_location %}, it exists as a remote repository. You can clone your repository to create a local copy on your computer and sync between the two locations.'
redirect_from:
  - /articles/cloning-a-repository
  - /articles/cloning-a-repository-from-github
  - /github/creating-cloning-and-archiving-repositories/cloning-a-repository
  - /github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
---

## Über das Klonen eines Repositorys

You can clone a repository from {% data variables.product.product_location %} to your local computer to make it easier to fix merge conflicts, add or remove files, and push larger commits. When you clone a repository, you copy the repository from {% data variables.product.product_location %} to your local machine.

Das Klonen eines Repository ruft eine vollständige Kopie aller Repository-Daten ab, die {% data variables.product.product_location %} zu diesem Zeitpunkt hat, inklusive aller Versionen jeder Datei und jedes Ordners für das Projekt. You can push your changes to the remote repository on {% data variables.product.product_location %}, or pull other people's changes from {% data variables.product.product_location %}. For more information, see "[Using Git](/github/getting-started-with-github/using-git)".

You can clone your existing repository or clone another person's existing repository to contribute to a project.

## Ein Repository klonen

{% include tool-switcher %}

{% webui %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.copy-clone-url %}
{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.command_line.change-current-directory-clone %}
{% data reusables.command_line.git-clone-url %}
{% data reusables.command_line.local-clone-created %}

{% endwebui %}

{% cli %}

{% data reusables.cli.cli-learn-more %}

To clone a repository locally, use the `repo clone` subcommand. Replace the `repository` parameter with the repository name. For example, `octo-org/octo-repo`, `monalisa/octo-repo`, or `octo-repo`. If the `OWNER/` portion of the `OWNER/REPO` repository argument is omitted, it defaults to the name of the authenticating user.

```shell
gh repo clone <em>repository</em>
```

You can also use the GitHub URL to clone a repository.

```shell
gh repo clone <em>https://github.com/cli/cli</em>
```

{% endcli %}

{% desktop %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.open-with-github-desktop %}
4. Befolgen Sie die Aufforderungen in {% data variables.product.prodname_desktop %}, um den Klonvorgang abzuschließen.

Weitere Informationen finden Sie unter „[Ein Repository von {% data variables.product.prodname_dotcom %} in {% data variables.product.prodname_desktop %} klonen](/desktop/guides/contributing-to-projects/cloning-a-repository-from-github-to-github-desktop/)“.

{% enddesktop %}

## Ein leeres Repository klonen

Ein leeres Repository enthält keine Dateien. Dies geschieht öfters, wenn Du das Repository bei der Erstellung nicht mit einer README-Datei initialisierst.

{% data reusables.repositories.navigate-to-repo %}
2. Um Dein Repository über die Befehlszeile mit HTTPS zu klonen, klicke unter „Quick setup" (Schnelleinrichtung) auf {% octicon "clippy" aria-label="The clipboard icon" %}. To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority, click **SSH**, then click {% octicon "clippy" aria-label="The clipboard icon" %}. ![Schaltfläche „Empty repository clone URL" (Leeres-Repository-Klonen-URL)](/assets/images/help/repository/empty-https-url-clone-button.png)

   Um Dein Repository alternativ in Desktop zu klonen, klicke {% octicon "desktop-download" aria-label="The desktop download button" %} **Set up in Desktop** (In Desktop aufsetzen) und folge den Anweisungen, um den Klon zu vervollständigen. ![Schaltfläche „Empty repository desktop" (Leeres-Repository-Klonen-Desktop)](/assets/images/help/repository/empty-desktop-clone-button.png)

{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.command_line.change-current-directory-clone %}
{% data reusables.command_line.git-clone-url %}
{% data reusables.command_line.local-clone-created %}

## Beheben von Fehlern beim Klonen

Beim Klonen eines Repositorys wirst Du allenfalls Fehlern begegnen.

Wenn Du ein Repository nicht klonen kannst, überprüfe Folgendes:

- Du kannst zu HTTPS verbinden. Weitere Informationen findest Du unter „[Fehler beim HTTPS-Klonen](/github/creating-cloning-and-archiving-repositories/https-cloning-errors)."
- Du hast die Berechtigung zum Zugriff auf das Repository, das Du klonen willst. Weitere Informationen findest du auf „[Error: Repository not found](/github/creating-cloning-and-archiving-repositories/error-repository-not-found)" (Fehler: Repository nicht gefunden).
- Der Standardbranch, den Du klonen willst, existiert immer noch. Für weitere Informationen, prüfe, ob Du die Berechtigungen zum Zugriff auf das zu klonende Repository hast. Weitere Informationen findest Du unter „[Error: Remote HEAD refers to nonexistent ref, unable to checkout](/github/creating-cloning-and-archiving-repositories/error-remote-head-refers-to-nonexistent-ref-unable-to-checkout)" (Fehler: HEAD des Remote enthält eine nicht existierende Referenz, auschecken nicht möglich).

{% ifversion fpt or ghec %}

## Weiterführende Informationen

- „[Verbindungsprobleme beheben](/articles/troubleshooting-connectivity-problems)“
{% endif %}
