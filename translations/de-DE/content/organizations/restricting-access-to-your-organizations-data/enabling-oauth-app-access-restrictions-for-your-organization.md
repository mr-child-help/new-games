---
title: OAuth-App-Zugriffsbeschränkungen für Deine Organisation aktivieren
intro: 'Organization owners can enable {% data variables.product.prodname_oauth_app %} access restrictions to prevent untrusted apps from accessing the organization''s resources while allowing organization members to use {% data variables.product.prodname_oauth_apps %} for their personal accounts.'
redirect_from:
  - /articles/enabling-third-party-application-restrictions-for-your-organization/
  - /articles/enabling-oauth-app-access-restrictions-for-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/enabling-oauth-app-access-restrictions-for-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Enable OAuth App
---

{% data reusables.organizations.oauth_app_restrictions_default %}

{% warning %}

**Warnings**:
- Enabling {% data variables.product.prodname_oauth_app %} access restrictions will revoke organization access for all previously authorized {% data variables.product.prodname_oauth_apps %} and SSH keys. Weitere Informationen findest Du unter „[Informationen zu {% data variables.product.prodname_oauth_app %}-Zugriffsbeschränkungen](/articles/about-oauth-app-access-restrictions).“
- Wenn Sie die {% data variables.product.prodname_oauth_app %}-Zugriffseinschränkungen eingerichtet haben, stellen Sie sicher, dass Sie alle {% data variables.product.prodname_oauth_app %}s erneut autorisieren, die regelmäßig Zugriff auf die privaten Daten der Organisation benötigen. Alle Organisationsmitglieder müssen neue SSH-Schlüssel erstellen, und die Organisation muss nach Bedarf neue Deployment-Schlüssel erstellen.
- Wenn {% data variables.product.prodname_oauth_app %}-Zugriffseinschränkungen aktiviert sind, können Anwendungen mit einem OAuth-Token auf Informationen zu {% data variables.product.prodname_marketplace %}-Transaktionen zugreifen.

{% endwarning %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.oauth_app_access %}
5. Klicke unter „Third-party application access policy“ (Zugriffsrichtlinie für Drittanbieter-Anwendungen) auf **Setup application access restrictions** (Zugriffsbeschränkungen für Anwendungen einrichten). ![Schaltfläche „Set up restrictions" (Einrichten von Beschränkungen)](/assets/images/help/settings/settings-third-party-set-up-restrictions.png)
6. Wenn Du die Informationen zu Drittanbieter-Zugriffsbeschränkungen gelesen hast, klicke auf **Restrict third-party application access** (Zugriff von Drittanbieter-Anwendungen beschränken). ![Schaltfläche „Restriction confirmation" (Beschränkungen bestätigen)](/assets/images/help/settings/settings-third-party-restrict-confirm.png)
