---
title: Verwalten der Forking-Richtlinie für Dein Repository
intro: 'Du kannst das Forken eines bestimmten privaten{% ifversion fpt or ghae or ghes or ghec %} oder internen{% endif %} Repositorys einer Organisation erlauben oder verhindern.'
redirect_from:
  - /articles/allowing-people-to-fork-a-private-repository-owned-by-your-organization
  - /github/administering-a-repository/allowing-people-to-fork-a-private-repository-owned-by-your-organization
  - /github/administering-a-repository/managing-the-forking-policy-for-your-repository
  - /github/administering-a-repository/managing-repository-settings/managing-the-forking-policy-for-your-repository
permissions: People with admin permissions for a repository can manage the forking policy for the repository.
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
shortTitle: Die Forking-Richtlinie verwalten
---

Ein Organisationsinhaber muss Forks von privaten{% ifversion fpt or ghae or ghes or ghec %} und internen{% endif %} Repositorys auf der Organisationsebene erlauben, bevor Du Forks für ein bestimmtes Repository erlauben oder verbieten kannst. Weitere Informationen findest Du unter „[Die Forking-Richtlinie für Deine Organisation verwalten](/organizations/managing-organization-settings/managing-the-forking-policy-for-your-organization)."

{% data reusables.organizations.internal-repos-enterprise %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
3. Wähle unter „Features“ (Funktionen) **Allow forking** (Forking erlauben) aus. ![Kontrollkästchen, um das Forking eines privaten Repositorys zu erlauben oder zu verbieten](/assets/images/help/repository/allow-forking-specific-org-repo.png)

## Weiterführende Informationen

- „[Informationen zu Forks](/articles/about-forks)“
- "[Repository roles for an organization](/organizations/managing-access-to-your-organizations-repositories/repository-roles-for-an-organization)"
