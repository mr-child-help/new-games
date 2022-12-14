---
title: Eine Zahlungsmethode hinzufügen oder bearbeiten
intro: Du kannst jederzeit eine Zahlungsmethode zu Deinem Konto hinzufügen oder die vorhandene Zahlungsmethode für Dein Konto aktualisieren.
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/adding-or-editing-a-payment-method
  - /articles/updating-your-personal-account-s-payment-method/
  - /articles/how-do-i-update-my-credit-card/
  - /articles/updating-your-account-s-credit-card/
  - /articles/updating-your-personal-account-s-credit-card/
  - /articles/updating-your-personal-account-s-paypal-information/
  - /articles/does-github-provide-invoicing/
  - /articles/switching-payment-methods-for-your-personal-account/
  - /articles/paying-for-your-github-organization-account/
  - /articles/updating-your-organization-s-credit-card/
  - /articles/updating-your-organization-s-paypal-information/
  - /articles/updating-your-organization-s-payment-method/
  - /articles/switching-payment-methods-for-your-organization/
  - /articles/adding-or-editing-a-payment-method
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-your-github-billing-settings/adding-or-editing-a-payment-method
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Organizations
  - User account
shortTitle: Manage a payment method
---

{% data reusables.dotcom_billing.payment-methods %} {% data reusables.dotcom_billing.same-payment-method %}

Wir bieten keine Abrechnung und unterstützen keine Bestellungen für persönliche Konten. Wir versenden Quittungen monatlich oder jährlich zum Abrechnungsdatum Deines Kontos per E-Mail. Wenn Dein Unternehmen, Dein Land oder Deine Buchhaltung vorgibt, dass Quittungen detailliertere Angaben aufweisen müssen, kannst Du auch [zusätzliche Informationen zu Quittungen hinzufügen](/articles/adding-information-to-your-personal-account-s-receipts).

## Die Zahlungsmethode für Dein persönliches Konto aktualisieren

{% data reusables.user_settings.billing_plans %}
{% data reusables.dotcom_billing.update_payment_method %}
1. If your account has existing billing information that you want to update, click **Edit**. ![Billing New Card button](/assets/images/help/billing/billing-information-edit-button.png)
{% data reusables.dotcom_billing.enter-billing-info %}
1. If your account has an existing payment method that you want to update, click **Edit**. ![Billing New Card button](/assets/images/help/billing/billing-payment-method-edit-button.png)
{% data reusables.dotcom_billing.enter-payment-info %}

## Die Zahlungsmethode für Deine Organisation aktualisieren

{% data reusables.dotcom_billing.org-billing-perms %}

Wenn sich Deine Organisation außerhalb der USA befindet oder Du zum Bezahlen von {% data variables.product.product_name %} ein Firmenkonto verwendest, bietet sich PayPal als Zahlungsmethode an.

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.update_payment_method %}
1. If your account has an existing credit card that you want to update, click **New Card**. ![Billing New Card button](/assets/images/help/billing/billing-new-card-button.png)
{% data reusables.dotcom_billing.enter-payment-info %}
