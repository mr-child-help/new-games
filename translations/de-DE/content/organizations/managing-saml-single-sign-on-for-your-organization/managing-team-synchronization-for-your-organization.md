---
title: Teamsynchronisierung für Deine Organisation verwalten
intro: 'Du kannst die Teamsynchronisierung zwischen Deinem Identitätsanbieter (IdP) und Deiner Organisation auf {% data variables.product.product_name %} aktivieren oder deaktivieren.'
product: '{% data reusables.gated-features.team-synchronization %}'
redirect_from:
  - /articles/synchronizing-teams-between-your-identity-provider-and-github
  - /github/setting-up-and-managing-organizations-and-teams/synchronizing-teams-between-your-identity-provider-and-github
  - /github/articles/synchronizing-teams-between-okta-and-github
  - /github/setting-up-and-managing-organizations-and-teams/managing-team-synchronization-for-your-organization
permissions: Organization owners can manage team synchronization for an organization.
miniTocMaxHeadingLevel: 3
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Manage team synchronization
---

{% data reusables.enterprise-accounts.emu-scim-note %}

{% data reusables.gated-features.okta-team-sync %}

## Informationen zur Teamsynchronisierung

Du kannst die Teamsynchronisierung zwischen Deinem IdP und {% data variables.product.product_name %} aktivieren, um es den Organisationsinhabern und Team-Betreuern zu ermöglichen, Teams in Deiner Organisation mit IdP-Gruppen zu verbinden.

{% data reusables.identity-and-permissions.about-team-sync %}

{% data reusables.identity-and-permissions.supported-idps-team-sync %}

{% data reusables.identity-and-permissions.sync-team-with-idp-group %}

Du kannst die Teamsynchronisierung auch für Organisationen im Besitz eines Enterprise-Kontos aktivieren. For more information, see "[Managing team synchronization for organizations in your enterprise](/enterprise-cloud@latest/admin/authentication/managing-identity-and-access-for-your-enterprise/managing-team-synchronization-for-organizations-in-your-enterprise)."

{% data reusables.enterprise-accounts.team-sync-override %}

{% data reusables.identity-and-permissions.team-sync-usage-limits %}

## Teamsynchronisierung aktivieren

Die Schritte zur Aktivierung der Teamsynchronisierung hängen vom IdP ab, den Du verwenden möchtest. Es gibt Voraussetzungen zur Aktivierung der Teamsynchronisierung, die auf jeden IdP zutreffen. Jeder einzelne IdP hat zusätzliche Voraussetzungen.

### Vorrausetzungen

{% data reusables.identity-and-permissions.team-sync-required-permissions %}

Du musst SAML Single Sign-On für Deine Organisation und Deinen unterstützten IdP aktivieren. Weitere Informationen findest Du unter „[SAML Single Sign-On für Deine Organisation erzwingen](/articles/enforcing-saml-single-sign-on-for-your-organization).“

Du musst Dich für Deine Organisation mittels SAML SSO und dem unterstützten IdP authentifizieren. Weitere Informationen findest Du unter „[Authentifizierung mit SAML Single Sign-On](/articles/authenticating-with-saml-single-sign-on).“

### Teamsynchronisierung für Azure AD aktivieren

{% data reusables.identity-and-permissions.team-sync-azure-permissions %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
{% data reusables.identity-and-permissions.team-sync-confirm-saml %}
{% data reusables.identity-and-permissions.enable-team-sync-azure %}
{% data reusables.identity-and-permissions.team-sync-confirm %}
6. Prüfe die Mandanteninformationen des Identitätsanbieters für Deine Organisation, und klicke auf **Approve** (Genehmigen). ![Ausstehende Anforderung zum Aktivieren der Teamsynchronisierung für einen IdP-Mandanten mit der Option zur Genehmigung oder Ablehnung](/assets/images/help/teams/approve-team-synchronization.png)

### Teamsynchronisierung für Okta aktivieren

{% data reusables.identity-and-permissions.team-sync-okta-requirements %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
{% data reusables.identity-and-permissions.team-sync-confirm-saml %}
{% data reusables.identity-and-permissions.enable-team-sync-okta %}
7. Gib unterhalb dem Namen Deiner Organisation einen gültigen SSWS-Token und die URL zu Deiner Okta-Instanz ein. ![Okta Organisationsformular für das Aktivieren der Teamsynchronisierung](/assets/images/help/teams/confirm-team-synchronization-okta-organization.png)
6. Überprüfe die Mandanteninformationen des Identitätsanbieters, den Du mit Deiner Organisation verbinden möchtest und klicke auf **Approve** (Genehmigen). ![Schaltfläche „Enable team synchronization" (Teamsynchronisierung aktivieren)](/assets/images/help/teams/confirm-team-synchronization-okta.png)

## Teamsynchronisierung deaktivieren

{% data reusables.identity-and-permissions.team-sync-disable %}

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
5. Klicke unter „Team synchronization“ (Teamsynchronisierung) auf **Disable team synchronization** (Teamsynchronisierung deaktivieren). ![Deaktivieren der Teamsynchronisierung](/assets/images/help/teams/disable-team-synchronization.png)
