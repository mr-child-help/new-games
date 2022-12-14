---
title: Die Forking-Richtlinie für Deine Organisation verwalten
intro: 'You can allow or prevent the forking of any private{% ifversion fpt or ghes or ghae or ghec %} and internal{% endif %} repositories owned by your organization.'
redirect_from:
  - /articles/allowing-people-to-fork-private-repositories-in-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/allowing-people-to-fork-private-repositories-in-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/managing-the-forking-policy-for-your-organization
permissions: Organization owners can manage the forking policy for an organization.
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Manage forking policy
---

Standardmäßig sind neue Organisationen so konfiguriert, dass sie das Forken von privaten{% ifversion fpt or ghes or ghae or ghec %} und internen{% endif %} Repositorys verbieten.

Wenn Du das Forken von privaten{% ifversion fpt or ghes or ghae or ghec %} und internen{% endif %} Repositorys auf Organisationsebene zulässt, kannst Du auch die Möglichkeit konfigurieren, ein bestimmtes privates{% ifversion fpt or ghes or ghae or ghec %} oder internes{% endif %} Repository zu forken. Weitere Informationen findest Du unter „[Die Forking-Richtlinie für Dein Repository verwalten](/github/administering-a-repository/managing-the-forking-policy-for-your-repository)."

{% data reusables.organizations.internal-repos-enterprise %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.member-privileges %}
5. Wähle unter „Repository forking" (Forken eines Repositorys) die Option **Allow forking of private repositories** (das Forken von privaten Repositorys zulassen) oder die Option **Allow forking of private and internal repositories** (Forking von privaten und internen Repositorys zulassen). ![Kontrollkästchen, um das Forking in der Organisation zu erlauben oder zu verbieten](/assets/images/help/repository/allow-disable-forking-organization.png)
6. Klicke auf **Save** (Speichern).

## Weiterführende Informationen

- „[Informationen zu Forks](/articles/about-forks)“
- "[Repository roles for an organization](/organizations/managing-access-to-your-organizations-repositories/repository-roles-for-an-organization)"
