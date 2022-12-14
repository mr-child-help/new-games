---
title: Informationen zu Releases
intro: 'Du kannst einen Release erstellen, um Software zusammen mit Release-Hinweisen und Links zu Binärdateien zu paketieren, damit sie von anderen Personen verwendet werden kann.'
redirect_from:
  - /articles/downloading-files-from-the-command-line/
  - /articles/downloading-files-with-curl/
  - /articles/about-releases
  - /articles/getting-the-download-count-for-your-releases
  - /github/administering-a-repository/getting-the-download-count-for-your-releases
  - /github/administering-a-repository/about-releases
  - /github/administering-a-repository/releasing-projects-on-github/about-releases
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
---

## Informationen zu Releases

{% ifversion fpt or ghec or ghes > 3.4 or ghae-issue-4974 %}
![Ein Überblick der Releases](/assets/images/help/releases/refreshed-releases-overview-with-contributors.png)
{% elsif ghes > 3.2 or ghae-issue-4972 %}
![Ein Überblick der Releases](/assets/images/help/releases/releases-overview-with-contributors.png)
{% else %}
![Ein Überblick der Releases](/assets/images/help/releases/releases-overview.png)
{% endif %}

Releases sind einsetzbare Software-Iterationen, die Du paketieren und für ein breiteres Publikum zum Herunterladen und Nutzen zur Verfügung stellen kannst.

Releases basieren auf [Git-Tags](https://git-scm.com/book/en/Git-Basics-Tagging), die einen bestimmten Punkt im Verlauf Deines Repositorys kennzeichnen. Ein Tag kann ein anderes Datum haben als ein Release, da sie zu unterschiedlichen Zeiten erstellt wurden. Weitere Informationen zum Anzeigen Deiner vorhandenen Tags findest Du unter „[Anzeigen der Releases und Tags Deines Repositorys](/github/administering-a-repository/viewing-your-repositorys-releases-and-tags)."

Du kannst Benachrichtigungen erhalten, wenn neue Releases in einem Repository verfügbar sind, ohne Benachrichtigungen über andere Updates des gleichen Repositorys zu erhalten. Weitere Informationen findest Du unter {% ifversion fpt or ghae or ghes or ghec %}„[Anzeigen Deiner Abonnements](/github/managing-subscriptions-and-notifications-on-github/viewing-your-subscriptions){% else %}„[Anzeige von Releases für ein Repository aktivieren oder deaktivieren](/github/receiving-notifications-about-activity-on-github/watching-and-unwatching-releases-for-a-repository){% endif %}."

Alle Personen mit Lesezugriff auf ein Repository können Releases anzeigen und vergleichen, aber nur Personen mit Schreibberechtigungen für ein Repository können Releases verwalten. Weitere Informationen findest Du unter „[Verwalten von Releases in einem Repository](/github/administering-a-repository/managing-releases-in-a-repository)."

{% ifversion fpt or ghec %}

You can manually create release notes while managing a release. Alternatively, you can automatically generate release notes from a default template, or customize your own release notes template. For more information, see "[Automatically generated release notes](/repositories/releasing-projects-on-github/automatically-generated-release-notes)."

People with admin permissions to a repository can choose whether {% data variables.large_files.product_name_long %} ({% data variables.large_files.product_name_short %}) objects are included in the ZIP files and tarballs that {% data variables.product.product_name %} creates for each release. For more information, see "[Managing {% data variables.large_files.product_name_short %} objects in archives of your repository](/github/administering-a-repository/managing-git-lfs-objects-in-archives-of-your-repository)."
{% endif %}

{% ifversion fpt or ghec %}
If a release fixes a security vulnerability, you should publish a security advisory in your repository. {% data variables.product.prodname_dotcom %} reviews each published security advisory and may use it to send {% data variables.product.prodname_dependabot_alerts %} to affected repositories. For more information, see "[About GitHub Security Advisories](/github/managing-security-vulnerabilities/about-github-security-advisories)."

You can view the **Dependents** tab of the dependency graph to see which repositories and packages depend on code in your repository, and may therefore be affected by a new release. For more information, see "[About the dependency graph](/github/visualizing-repository-data-with-graphs/about-the-dependency-graph)."
{% endif %}

Du kannst auch das Release-API verwenden, um Informationen zu sammeln, wie zum Beispiel die Anzahl der Downloads eines Release-Objekts. For more information, see "[Releases](/rest/reference/repos#releases)."

{% ifversion fpt or ghec %}
## Speicher- und Bandbreiten-Kontingente

 Jede Datei eines Release muss kleiner sein als {% data variables.large_files.max_file_size %}. Es gibt keine Begrenzung für die Gesamtgröße eines Release oder die Bandbreitennutzung.

{% endif %}
