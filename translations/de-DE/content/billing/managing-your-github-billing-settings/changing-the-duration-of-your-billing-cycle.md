---
title: Die Dauer des Abrechnungszeitraums ändern
intro: Für die Bezahlung des Abonnements und anderer bezahlter Funktionen Deines Kontos kannst Du einen monatlichen oder jährlichen Abrechnungszeitraum auswählen.
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/changing-the-duration-of-your-billing-cycle
  - /articles/monthly-and-yearly-billing/
  - /articles/switching-between-monthly-and-yearly-billing-for-your-personal-account/
  - /articles/switching-between-monthly-and-yearly-billing-for-your-organization/
  - /articles/changing-the-duration-of-your-billing-cycle
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-your-github-billing-settings/changing-the-duration-of-your-billing-cycle
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Organizations
  - Repositories
  - User account
shortTitle: Billing cycle
---

Wenn Sie die Dauer Ihres Abrechnungszeitraums ändern, werden Ihr {% data variables.product.prodname_dotcom %}-Abonnement und alle weiteren bezahlten Features und Produkte am nächsten Abrechnungsdatum auf den neuen Abrechnungszeitraum umgestellt.

## Die Dauer des Abrechnungszeitraums Deines persönlichen Kontos ändern

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.billing_plans %}
{% data reusables.dotcom_billing.change_plan_duration %}
{% data reusables.dotcom_billing.confirm_duration_change %}

## Die Dauer des Abrechnungszeitraums Deiner Organisation ändern

{% data reusables.dotcom_billing.org-billing-perms %}

### Die Dauer eines benutzerabhängigen Abonnements ändern

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.change_plan_duration %}
{% data reusables.dotcom_billing.confirm_duration_change %}

### Die Dauer eines alten Repository-abhängigen Plans ändern

{% data reusables.organizations.billing-settings %}
4. Klicke unter „Billing overview“ (Abrechnungsübersicht) auf **Change plan** (Plan ändern). ![Schaltfläche zum Ändern des Plans in der Abrechnungsübersicht](/assets/images/help/billing/billing_overview_change_plan.png)
5. Klicke in der oberen rechten Ecke auf **Switch to monthly billing** (Auf monatliche Abrechnung umstellen) oder **Switch to yearly billing** (Auf jährliche Abrechnung umstellen). ![Abschnitt zu Abrechnungsinformationen](/assets/images/help/billing/settings_billing_organization_plans_switch_to_yearly.png)
