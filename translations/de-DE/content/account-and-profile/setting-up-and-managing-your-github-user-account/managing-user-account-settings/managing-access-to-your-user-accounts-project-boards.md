---
title: Zugriff auf die Projektboards Deines Benutzerkontos verwalten
intro: Als Projektboard-Inhaber kannst Du einen Mitarbeiter hinzufügen oder entfernen und seine Berechtigungen für das Projektboard anpassen.
redirect_from:
  - /articles/managing-project-boards-in-your-repository-or-organization/
  - /articles/managing-access-to-your-user-account-s-project-boards
  - /articles/managing-access-to-your-user-accounts-project-boards
  - /github/setting-up-and-managing-your-github-user-account/managing-access-to-your-user-accounts-project-boards
  - /github/setting-up-and-managing-your-github-user-account/managing-user-account-settings/managing-access-to-your-user-accounts-project-boards
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Accounts
shortTitle: Manage access project boards
---

Ein Mitarbeiter ist eine Person, die Berechtigungen für eines Deiner Projektboards besitzt. Die Berechtigung eines Mitarbeiters ist standardmäßig der Lesezugriff. Weitere Informationen findest Du unter „[Berechtigungsebenen für Benutzer-Projektboards](/articles/permission-levels-for-user-owned-project-boards).“

## Mitarbeiter in ein Benutzer-Projektboard einladen

1. Navigiere zu dem Projektboard, zu dem Du einen Mitarbeiter hinzufügen möchtest.
{% data reusables.project-management.click-menu %}
{% data reusables.project-management.access-collaboration-settings %}
{% data reusables.project-management.collaborator-option %}
5. Geben Sie unter „Search by username, full name or email address“ (Nach Benutzernamen, vollständigem Namen oder E-Mail-Adresse suchen) den Namen, den Benutzernamen oder die {% data variables.product.prodname_dotcom %}-E-Mail-Adresse des Mitarbeiters ein. ![Der Bereich „Collaborators“ (Mitarbeiter) mit Octocat-Benutzernamen im Suchfeld](/assets/images/help/projects/org-project-collaborators-find-name.png)
{% data reusables.project-management.add-collaborator %}
7. Der neue Mitarbeiter besitzt standardmäßig Leseberechtigung. Wähle optional im Dropdownmenü neben dem Namen des neuen Mitarbeiters eine andere Berechtigungsebene aus. ![Der Mitarbeiter-Bereich mit ausgewähltem Berechtigungs-Dropdownmenü](/assets/images/help/projects/user-project-collaborators-edit-permissions.png)

## Mitarbeiter aus einem Benutzer-Projektboard entfernen

{% data reusables.project-management.click-menu %}
{% data reusables.project-management.access-collaboration-settings %}
{% data reusables.project-management.collaborator-option %}
{% data reusables.project-management.remove-collaborator %}
