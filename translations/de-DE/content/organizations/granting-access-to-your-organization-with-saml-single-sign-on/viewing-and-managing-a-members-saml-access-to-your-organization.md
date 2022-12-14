---
title: SAML-Zugriff eines Mitglieds auf Deine Organisation ansehen und verwalten
intro: 'Du kannst die verknüpfte Identität, aktive Sitzungen und autorisierte Anmeldeinformationen eines Organisations-Mitglieds ansehen und widerrufen.'
permissions: Organization owners can view and manage a member's SAML access to an organization.
product: '{% data reusables.gated-features.saml-sso %}'
redirect_from:
  - /articles/viewing-and-revoking-organization-members-authorized-access-tokens
  - /github/setting-up-and-managing-organizations-and-teams/viewing-and-revoking-organization-members-authorized-access-tokens
  - /github/setting-up-and-managing-organizations-and-teams/viewing-and-managing-a-members-saml-access-to-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Manage SAML access
---

## Über SAML Zugriff auf Deine Organisation

When you enable SAML single sign-on for your organization, each organization member can link their external identity on your identity provider (IdP) to their existing account on {% data variables.product.product_location %}. Um auf die Ressourcen Deiner Organisation auf {% data variables.product.product_name %} zuzugreifen, muss das Mitglied eine aktive SAML-Sitzung in seinem Browser haben. Um über API und Git auf die Ressourcen Deiner Organisation zugreifen zu können, muss das Mitglied ein persönliches Zugriffstoken oder einen SSH-Schlüssel verwenden, den das Mitglied für die Verwendung mit Deiner Organisation autorisiert hat.

Du kannst die verknüpfte Identität, die aktiven Sitzungen und die autorisierten Anmeldeinformationen auf der gleichen Seite anzeigen und widerrufen.

## Eine verknüpfte Identität anschauen und widerrufen

{% data reusables.saml.about-linked-identities %}

Wenn verfügbar, wird der Eintrag SCIM-Daten enthalten. Weitere Informationen findest Du unter „[Über SCIM](/organizations/managing-saml-single-sign-on-for-your-organization/about-scim)."

{% warning %}

**Warning:** For organizations using SCIM:
- Revoking a linked user identity on {% data variables.product.product_name %} will also remove the SAML and SCIM metadata. As a result, the identity provider will not be able to synchronize or deprovision the linked user identity.
- An admin must revoke a linked identity through the identity provider.
- To revoke a linked identity and link a different account through the identity provider, an admin can remove and re-assign the user to the {% data variables.product.product_name %} application. For more information, see your identity provider's documentation.

{% endwarning %}


{% data reusables.identity-and-permissions.revoking-identity-team-sync %}

{% data reusables.profile.access_org %}
{% data reusables.user_settings.access_org %}
{% data reusables.organizations.people %}
{% data reusables.saml.click-person-revoke-identity %}
{% data reusables.saml.saml-identity-linked %}
{% data reusables.saml.view-sso-identity %}
{% data reusables.saml.revoke-sso-identity %}
{% data reusables.saml.confirm-revoke-identity %}

## Eine aktive SAML-Sitzung ansehen und widerrufen

{% data reusables.profile.access_org %}
{% data reusables.user_settings.access_org %}
{% data reusables.organizations.people %}
{% data reusables.saml.click-person-revoke-session %}
{% data reusables.saml.saml-identity-linked %}
{% data reusables.saml.view-saml-sessions %}
{% data reusables.saml.revoke-saml-session %}

## Autorisierte Anmeldeinformationen anschauen und widerrufen

{% data reusables.saml.about-authorized-credentials %}

{% data reusables.profile.access_org %}
{% data reusables.user_settings.access_org %}
{% data reusables.organizations.people %}
{% data reusables.saml.click-person-revoke-credentials %}
{% data reusables.saml.saml-identity-linked %}
{% data reusables.saml.view-authorized-credentials %}
{% data reusables.saml.revoke-authorized-credentials %}
{% data reusables.saml.confirm-revoke-credentials %}

## Weiterführende Informationen

- "[About identity and access management with SAML single sign-on](/articles/about-identity-and-access-management-with-saml-single-sign-on)"{% ifversion ghec %}
- "[Viewing and managing a user's SAML access to your enterprise account](/admin/user-management/managing-users-in-your-enterprise/viewing-and-managing-a-users-saml-access-to-your-enterprise)"{% endif %}
