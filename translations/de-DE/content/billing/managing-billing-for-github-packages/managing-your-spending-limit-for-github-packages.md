---
title: Dein Ausgabenlimit für GitHub Packages verwalten
intro: 'Du kannst ein Ausgabenlimit für {% data variables.product.prodname_registry %} festlegen.'
product: '{% data reusables.gated-features.packages %}'
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-your-spending-limit-for-github-packages
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-billing-for-github-packages/managing-your-spending-limit-for-github-packages
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Enterprise
  - Organizations
  - Packages
  - Spending limits
  - User account
shortTitle: Your spending limit
---

## Über Ausgabenlimits für {% data variables.product.prodname_registry %}

{% data reusables.package_registry.packages-billing %}

{% data reusables.package_registry.packages-spending-limit-brief %}

{% data reusables.actions.actions-packages-set-spending-limit %} For more information about pricing for {% data variables.product.prodname_registry %} usage, see "[About billing for {% data variables.product.prodname_registry %}](/billing/managing-billing-for-github-packages/about-billing-for-github-packages)."

{% ifversion ghec %}
If you purchased {% data variables.product.prodname_enterprise %} through a Microsoft Enterprise Agreement, you can connect your Azure Subscription ID to your enterprise account to enable and pay for {% data variables.product.prodname_registry %} usage beyond the amounts including with your account. For more information, see "[Connecting an Azure subscription to your enterprise](/billing/managing-billing-for-your-github-account/connecting-an-azure-subscription-to-your-enterprise)."
{% endif %}

As soon as you set a spending limit other than $0, you will be responsible for any existing overages in the current billing period. Wenn Dein Unternehmen beispielsweise {% data variables.product.prodname_team %} verwendet, keine Überschreitungen zulässt, und Workflow-Artefakte erstellt, die Deinen Speicherverbrauch für den Monat von 1,9 GB auf 2,1 GB erhöht, wird die Veröffentlichung leicht mehr Speicher als die 2 GB nutzen, die Dein Produkt enthält.

Da Du keine Überschreitungen zugelassen hast, wird Dein nächster Versuch, eine Version des Pakets zu veröffentlichen, fehlschlagen. Du wirst keine Rechnung für die Überschreitung um 0,1 GB für diesen Monat erhalten. However, if you enable overages, your first bill will include the 0.1GB of existing overage for the current billing cycle, as well as any additional overages you accrue.

## Das Ausgabenlimit für {% data variables.product.prodname_registry %} für Dein Benutzerkonto verwalten

Jeder kann das Ausgabenlimit für {% data variables.product.prodname_registry %} für sein eigenes Benutzerkonto verwalten.

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.billing_plans %}
{% data reusables.dotcom_billing.manage-spending-limit %}
{% data reusables.dotcom_billing.monthly-spending-limit %}
{% data reusables.dotcom_billing.update-spending-limit %}

## Das Ausgabenlimit für {% data variables.product.prodname_registry %} für Deine Organisation verwalten

Organisationsinhaber und Abrechnungsmanager können das Ausgabenlimit von {% data variables.product.prodname_registry %} für eine Organisation verwalten.

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.manage-spending-limit %}
{% data reusables.dotcom_billing.monthly-spending-limit-actions-packages %}
{% data reusables.dotcom_billing.update-spending-limit %}

## Das Ausgabenlimit für {% data variables.product.prodname_registry %} für Dein Enterprise-Konto verwalten

Enterprise-Inhaber und Abrechnungsmanager können das Ausgabenlimit von {% data variables.product.prodname_registry %} für ein Enterprise-Konto verwalten.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.billing-tab %}
1. Above "{% data variables.product.prodname_actions %} and Packages monthly usage", click **Spending Limit**. ![Spending limit tab](/assets/images/help/settings/spending-limit-tab-enterprise.png)
{% data reusables.dotcom_billing.monthly-spending-limit %}
{% data reusables.dotcom_billing.update-spending-limit %}

## Managing usage and spending limit email notifications
{% data reusables.billing.email-notifications %}
