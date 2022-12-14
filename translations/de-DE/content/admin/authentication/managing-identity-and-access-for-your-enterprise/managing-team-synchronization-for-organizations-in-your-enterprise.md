---
title: Managing team synchronization for organizations in your enterprise
intro: 'You can enable team synchronization between an identity provider (IdP) and {% data variables.product.product_name %} to allow organizations owned by your enterprise account to manage team membership through IdP groups.'
product: '{% data reusables.gated-features.enterprise-accounts %}'
permissions: Enterprise owners can manage team synchronization for an enterprise account.
versions:
  ghec: '*'
type: how_to
topics:
  - Accounts
  - Enterprise
  - SSO
  - Teams
redirect_from:
  - /github/setting-up-and-managing-your-enterprise/managing-team-synchronization-for-organizations-in-your-enterprise-account
  - /github/setting-up-and-managing-your-enterprise/configuring-identity-and-access-management-for-your-enterprise-account/managing-team-synchronization-for-organizations-in-your-enterprise-account
shortTitle: Manage team synchronization
---

{% data reusables.enterprise-accounts.emu-scim-note %}

## About team synchronization for enterprise accounts

If you use Azure AD as your IdP, you can enable team synchronization for your enterprise account to allow organization owners and team maintainers to synchronize teams in the organizations owned by your enterprise accounts with IdP groups.

{% data reusables.identity-and-permissions.about-team-sync %}

{% data reusables.identity-and-permissions.sync-team-with-idp-group %}

{% data reusables.identity-and-permissions.team-sync-disable %}

Du kannst auch die Teamsynchronisation für eine einzelne Organisation konfigurieren und verwalten. Weitere Informationen findest Du unter „[Teamsynchronisation für Deine Organisation verwalten](/organizations/managing-saml-single-sign-on-for-your-organization/managing-team-synchronization-for-your-organization)."

{% data reusables.identity-and-permissions.team-sync-usage-limits %}

## Vorrausetzungen

müssen Du oder Dein Azure AD-Administrator ein Global-Administrator oder ein Privileged Role-Administrator in Azure AD sein.

You must enforce SAML single sign-on for organizations in your enterprise account with your supported IdP. For more information, see "[Configuring SAML single sign-on for your enterprise](/admin/authentication/managing-identity-and-access-for-your-enterprise/configuring-saml-single-sign-on-for-your-enterprise)."

musst Du mit SAML SSO und der unterstützten IdP zu Deinem Enterprise-Konto authentifizieren. Weitere Informationen findest Du unter „[Authentifizierung mit SAML Single Sign-On](/articles/authenticating-with-saml-single-sign-on).“

## Teamsynchronisation für Azure AD verwalten

{% data reusables.identity-and-permissions.team-sync-azure-permissions %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.security-tab %}
{% data reusables.identity-and-permissions.team-sync-confirm-saml %}
{% data reusables.identity-and-permissions.enable-team-sync-azure %}
{% data reusables.identity-and-permissions.team-sync-confirm %}
7. Review the details for the IdP tenant you want to connect to your enterprise account, then click **Approve**. ![Ausstehende Anforderung zum Aktivieren der Teamsynchronisierung für einen IdP-Mandanten mit der Option zur Genehmigung oder Ablehnung](/assets/images/help/teams/approve-team-synchronization.png)
8. Um die Teamsynchronisation zu deaktivieren, klicke auf **Disable team synchronization** (Teamsynchronisation deaktivieren). ![Deaktivieren der Teamsynchronisierung](/assets/images/help/teams/disable-team-synchronization.png)
