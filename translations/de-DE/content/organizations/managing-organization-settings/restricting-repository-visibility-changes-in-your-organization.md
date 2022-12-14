---
title: Sichtbarkeitsänderungen von Repositorys in Deiner Organisation einschränken
intro: Zum Schutz Deiner Organisationsdaten kannst Du die Berechtigungen für die Änderung der Sichtbarkeit von Repositorys in Deiner Organisation konfigurieren.
redirect_from:
  - /articles/restricting-repository-visibility-changes-in-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/restricting-repository-visibility-changes-in-your-organization
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Set visibility changes policy
---

You can restrict the ability to change repository visibility to organization owners only, or allow members with admin privileges for a repository to also change visibility.

{% warning %}

**Warning**: If enabled, this setting allows people with admin permissions to change an existing repository to any visibility, even if you do not allow that type of repository to be created. For more information about restricting the visibility of repositories during creation, see "[Restricting repository creation in your organization](/articles/restricting-repository-creation-in-your-organization)."

{% endwarning %}


{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.member-privileges %}
5. Deaktiviere unter „Repository visibility change“ (Änderung der Sichtbarkeit von Repositorys) das Kontrollkästchen **Allow members to change repository visibilities for this organization** (Mitgliedern die Änderung der Sichtbarkeit von Repositorys für diese Organisation erlauben). ![Kontrollkästchen zur Erlaubnis der Änderung der Sichtbarkeit von Repositorys durch Mitglieder](/assets/images/help/organizations/disallow-members-to-change-repo-visibility.png)
6. Klicke auf **Save** (Speichern).

## Weiterführende Informationen

- "[About repositories](/repositories/creating-and-managing-repositories/about-repositories#about-repository-visibility)"
