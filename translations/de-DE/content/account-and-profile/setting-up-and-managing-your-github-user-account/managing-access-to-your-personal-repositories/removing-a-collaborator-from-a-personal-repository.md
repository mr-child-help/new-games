---
title: Mitarbeiter aus einem persönlichen Repository entfernen
intro: 'Wenn Du einen Mitarbeiter aus Deinem Projekt entfernst, verliert er seinen Lese-/Schreibzugriff auf Dein Repository. Falls das Repository privat ist und die Person einen Fork erstellt hat, wird der Fork ebenfalls gelöscht.'
redirect_from:
  - /articles/how-do-i-remove-a-collaborator/
  - /articles/what-happens-when-i-remove-a-collaborator-from-my-private-repository/
  - /articles/removing-a-collaborator-from-a-private-repository/
  - /articles/deleting-a-private-fork-of-a-private-user-repository/
  - /articles/how-do-i-delete-a-fork-of-my-private-repository/
  - /articles/removing-a-collaborator-from-a-personal-repository
  - /github/setting-up-and-managing-your-github-user-account/removing-a-collaborator-from-a-personal-repository
  - /github/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/removing-a-collaborator-from-a-personal-repository
product: '{% data reusables.gated-features.user-repo-collaborators %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Accounts
  - Repositories
shortTitle: Remove a collaborator
---

## Forks privater Repositorys löschen

Beim Entfernen eines Mitarbeiters werden zwar dessen Forks privater Repositorys gelöscht, seine lokalen Klone Deiner Repositorys behält er aber.

## Mitarbeiterberechtigungen einer Person entfernen, die zu einem Repository beiträgt

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% ifversion fpt or ghec %}
{% data reusables.repositories.navigate-to-manage-access %}
4. Klicke rechts neben dem Mitarbeiter, den Du entfernen möchtest, auf {% octicon "trash" aria-label="The trash icon" %}. ![Schaltfläche „Remove collaborator" (Entfernen des Mitarbeiters)](/assets/images/help/repository/collaborator-remove.png)
{% else %}
3. Klicke auf der linken Seitenleiste auf **Collaborators & teams** (Mitarbeiter und Teams). ![Registerkarte „Collaborators" (Mitarbeiter)](/assets/images/help/repository/repo-settings-collaborators.png)
4. Klicke auf das **X** neben dem Mitarbeiter, den Du entfernen möchtest. ![Link „Remove“ (Entfernen)](/assets/images/help/organizations/Collaborator-Remove.png)
{% endif %}

## Weiterführende Informationen

- „[Organisationsmitglieder aus einem Team entfernen](/articles/removing-organization-members-from-a-team)“
- „[Externen Mitarbeiter von einem Organisations-Repository entfernen](/articles/removing-an-outside-collaborator-from-an-organization-repository)“
