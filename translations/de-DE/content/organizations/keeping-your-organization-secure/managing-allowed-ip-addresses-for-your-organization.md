---
title: Verwaltung erlaubter IP-Adressen für Deine Organisation
intro: 'Du kannst den Zugriff auf die Objekte Deiner Organisation einschränken, indem Du eine Liste von IP-Adressen konfigurierst, die zu einer Verbindung berechtigt sind.'
product: '{% data reusables.gated-features.allowed-ip-addresses %}'
redirect_from:
  - /github/setting-up-and-managing-organizations-and-teams/managing-allowed-ip-addresses-for-your-organization
versions:
  fpt: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Manage allowed IP addresses
---

Organisationsinhaber können erlaubte IP-Adressen für eine Organisation verwalten.

## Informationen zu zulässigen IP-Adressen

Du kannst den Zugriff auf Organisations-Objekte beschränken, indem Du eine Genehmigungsliste für bestimmte IP-Adressen konfigurierst. {% data reusables.identity-and-permissions.ip-allow-lists-example-and-restrictions %}

{% data reusables.identity-and-permissions.ip-allow-lists-cidr-notation %}

{% data reusables.identity-and-permissions.ip-allow-lists-enable %}

If you set up an allow list you can also choose to automatically add to your allow list any IP addresses configured for {% data variables.product.prodname_github_apps %} that you install in your organization. The creator of a {% data variables.product.prodname_github_app %} can configure an allow list for their application, specifying the IP addresses at which the application runs. By inheriting their allow list into yours, you avoid connection requests from the application being refused. For more information, see "[Allowing access by {% data variables.product.prodname_github_apps %}](#allowing-access-by-github-apps)."

Du kannst erlaubte IP-Adressen auch für die Organisationen in einem Enterprise-Konto konfigurieren. For more information, see "[Enforcing policies for security settings in your enterprise](/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-security-settings-in-your-enterprise)."

## Eine zulässige IP-Adresse hinzufügen

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-ip %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-description %}
{% data reusables.identity-and-permissions.ip-allow-lists-add-entry %}

## Zulässige IP-Adressen aktivieren

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
1. Wähle unter „IP allow list“ (Liste der zulässigen IP-Adressen) **Enable IP allow list** (Liste der zulässigen IP-Adressen aktivieren) aus. ![Kontrollkästchen, um IP-Adressen zuzulassen](/assets/images/help/security/enable-ip-allowlist-organization-checkbox.png)
1. Klicke auf **Save** (Speichern).

## Allowing access by {% data variables.product.prodname_github_apps %}

If you're using an allow list, you can also choose to automatically add to your allow list any IP addresses configured for {% data variables.product.prodname_github_apps %} that you install in your organization.

{% data reusables.identity-and-permissions.ip-allow-lists-address-inheritance %}

{% data reusables.apps.ip-allow-list-only-apps %}

For more information about how to create an allow list for a {% data variables.product.prodname_github_app %} you have created, see "[Managing allowed IP addresses for a GitHub App](/developers/apps/building-github-apps/managing-allowed-ip-addresses-for-a-github-app)."

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
1. Under "IP allow list", select **Enable IP allow list configuration for installed GitHub Apps**. ![Checkbox to allow GitHub App IP addresses](/assets/images/help/security/enable-ip-allowlist-githubapps-checkbox.png)
1. Klicke auf **Save** (Speichern).

## Eine zulässige IP-Adresse bearbeiten

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-entry %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-ip %}
{% data reusables.identity-and-permissions.ip-allow-lists-edit-description %}
1. Klicke auf **Update** (Aktualisieren).

## Eine zulässige IP-Adresse löschen

{% data reusables.profile.access_org %}
{% data reusables.profile.org_settings %}
{% data reusables.organizations.security %}
{% data reusables.identity-and-permissions.ip-allow-lists-delete-entry %}
{% data reusables.identity-and-permissions.ip-allow-lists-confirm-deletion %}

## {% data variables.product.prodname_actions %} mit einer IP-Zulassungsliste verwenden

{% ifversion ghae %}

{% data reusables.github-actions.ip-allow-list-hosted-runners %}

{% else %}

{% data reusables.github-actions.ip-allow-list-self-hosted-runners %}

{% endif %}
