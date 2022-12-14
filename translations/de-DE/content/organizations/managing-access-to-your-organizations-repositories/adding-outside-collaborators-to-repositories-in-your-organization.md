---
title: Externe Mitarbeiter zu Organisations-Repositorys hinzufügen
intro: 'Ein *externer Mitarbeiter* ist eine Person, die nicht explizit Mitglied Deiner Organisation ist, aber Lese-, Schreib- oder Administratorberechtigungen für mindestens ein Repository in Deiner Organisation besitzt.'
redirect_from:
  - /articles/adding-outside-collaborators-to-repositories-in-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/adding-outside-collaborators-to-repositories-in-your-organization
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Add outside collaborator
---

## About outside collaborators

{% data reusables.organizations.owners-and-admins-can %} externe Mitarbeiter zu einem Repository hinzufügen, es sei denn, ein Organisationsinhaber hat die Möglichkeit zum Einladen von Mitarbeitern eingeschränkt. Weitere Informationen findest Du unter „[Berechtigungen zum Hinzufügen von externen Mitarbeitern festlegen](/articles/setting-permissions-for-adding-outside-collaborators)."

{% data reusables.organizations.outside-collaborators-use-seats %}

{% ifversion not ghae %}
Wenn Deine Organisation [die Zwei-Faktor-Authentifizierung für Mitglieder und externe Mitarbeiter vorschreibt](/articles/requiring-two-factor-authentication-in-your-organization), müssen die Benutzer die Zwei-Faktor-Authentifizierung aktivieren, bevor sie Deine Einladung zur Zusammenarbeit an einem Repository der Organisation annehmen können.
{% endif %}

{% data reusables.organizations.outside_collaborator_forks %}

{% ifversion fpt %}
To further support your team's collaboration abilities, you can upgrade to {% data variables.product.prodname_ghe_cloud %}, which includes features like protected branches and code owners on private repositories. {% data reusables.enterprise.link-to-ghec-trial %}
{% endif %}

## Adding outside collaborators to a repository

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% ifversion fpt or ghec %}
{% data reusables.repositories.navigate-to-manage-access %}
{% data reusables.organizations.invite-teams-or-people %}
5. Beginne im Suchfeld den Namen der Person einzugeben, die Du einladen möchtest, dann klicke in der Liste der Übereinstimmungen auf einen Namen. ![Suchfeld für die Eingabe des Namens der Person, die Du zu einem Repository einladen willst](/assets/images/help/repository/manage-access-invite-search-field.png)
6. Wähle unter „Choose a role" (Wähle eine Rolle) die zu gewährenden Berechtigungen für die Person, dann klicke auf **Add NAME to REPOSITORY** (Füge NAME zum REPOSITORY hinzu). ![Berechtigungen für die Person auswählen](/assets/images/help/repository/manage-access-invite-choose-role-add.png)
{% else %}
5. Klicke auf der linken Seitenleiste auf **Collaborators & teams** (Mitarbeiter und Teams). ![Seitenleiste der Repository-Einstellungen, wobei „Collaborators & Teams“ (Mitarbeiter & Teams) hervorgehoben ist](/assets/images/help/repository/org-repo-settings-collaborators-and-teams.png)
6. Gib unter „Collaborators“ (Mitarbeiter) den Namen der Person ein, der Du Zugriff auf das Repository gewähren möchtest, und klicke dann auf **Add collaborator** (Mitarbeiter hinzufügen). ![Der Bereich „Collaborators“ (Mitarbeiter) mit Octocat-Benutzernamen im Suchfeld](/assets/images/help/repository/org-repo-collaborators-find-name.png)
7. Wähle neben dem Namen des neuen Mitarbeiters die gewünschte Berechtigungsebene aus: *Write* (Schreibberechtigung), *Read* (Leseberechtigung) oder *Admin* (Administratorberechtigungen). ![Die Repository-Berechtigungsauswahl](/assets/images/help/repository/org-repo-collaborators-choose-permissions.png)
{% endif %}
