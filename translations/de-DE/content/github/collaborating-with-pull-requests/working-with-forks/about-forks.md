---
title: Informationen zu Forks
intro: 'Ein Fork ist eine Kopie eines Repositorys, das Du verwaltest. Mit Forks kannst Du Änderungen an einem Projekt vornehmen, ohne dass sich dies auf das ursprüngliche Repository auswirkt. Du kannst Updates aus dem ursprünglichen Repository abrufen oder Änderungen mit Pull Requests an das Repository senden.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/working-with-forks/about-forks
  - /articles/about-forks
  - /github/collaborating-with-issues-and-pull-requests/about-forks
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

Das Forking eines Repositorys ist ähnlich wie das Kopieren eines Repositorys, mit zwei wesentlichen Unterschieden:

* Du kannst einen Pull Request verwenden, um Änderungen von Deiner benutzereigenen Fork zum ursprünglichen Repository, auch als *upstream* (vorgelagertes) Repository bekannt, vorzuschlagen.
* Du kannst Änderungen vom vorgelagerten Repository auf Deinen lokalen Fork übertragen, indem Du Deinen Fork mit dem vorgelagerten Repository synchronisierst.

{% data reusables.repositories.you-can-fork %}

{% ifversion fpt or ghec %}

If you're a member of a {% data variables.product.prodname_emu_enterprise %}, there are further restrictions on the repositories you can fork. {% data reusables.enterprise-accounts.emu-forks %} For more information, see "[About {% data variables.product.prodname_emus %}](/enterprise-cloud@latest/admin/authentication/managing-your-enterprise-users-with-your-identity-provider/about-enterprise-managed-users){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

{% endif %}

{% data reusables.repositories.desktop-fork %}

Das Löschen eines Forks wird das ursprüngliche vorgelagerte Repository nicht löschen. Du kannst beliebige Änderungen an Deiner Fork vornehmen – Mitarbeiter hinzufügen, Dateien umbenennen, {% data variables.product.prodname_pages %} generieren –, ohne Auswirkungen auf das Original.{% ifversion fpt or ghec %} Du kannst ein geforktes Repository nach dem Löschen nicht wiederherstellen. Weitere Informationen findest Du unter „[Ein gelöschtes Repository wiederherstellen](/articles/restoring-a-deleted-repository)“.{% endif %}

In Open-Source-Projekten werden Forks oft verwendet, um mehrfach Ideen oder Änderungen durchzuspielen, bevor sie an das vorgelagerte Repository zurückgesendet werden. Wenn Du Änderungen in Deiner benutzereigenen Fork vornimmst und einen Pull Request öffnest, die Deine Arbeit mit dem vorgelagerten Repository vergleicht, kannst Du jedem mit Push-Zugriff auf das vorgelagerte Repository die Erlaubnis geben, Änderungen in deinen Pull-Request-Branch zu übertragen. Dies beschleunigt die Zusammenarbeit, indem es den Repository-Betreuern erlaubt, Commits zu erstellen oder Tests vor dem Zusammenführen lokal aus einer benutzereigenen Fork zu Deinem Pull-Request-Branch auszuführen. Du kannst keine Push-Berechtigungen an eine Fork geben, die einer Organisation gehört.

{% data reusables.repositories.private_forks_inherit_permissions %}

If you want to create a new repository from the contents of an existing repository but don't want to merge your changes upstream in the future, you can duplicate the repository or, if the repository is a template, use the repository as a template. For more information, see "[Duplicating a repository](/articles/duplicating-a-repository)" and "[Creating a repository from a template](/articles/creating-a-repository-from-a-template)".

## Weiterführende Informationen

- „[Informationen zu gemeinschaftlichen Entwicklungsmodellen](/articles/about-collaborative-development-models)“
- „[Einen Pull Request von einem Fork erstellen](/articles/creating-a-pull-request-from-a-fork)“
- [Open-Source-Leitfäden](https://opensource.guide/){% ifversion fpt or ghec %}
- [{% data variables.product.prodname_learning %}]({% data variables.product.prodname_learning_link %}){% endif %}
