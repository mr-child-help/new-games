---
title: Dein GitHub-Abonnement hochstufen
intro: 'You can upgrade the subscription for any type of account on {% data variables.product.product_location %} at any time.'
redirect_from:
  - /github/setting-up-and-managing-billing-and-payments-on-github/upgrading-your-github-subscription
  - /articles/upgrading-your-personal-account-s-billing-plan/
  - /articles/upgrading-your-personal-account/
  - /articles/upgrading-your-personal-account-from-free-to-a-paid-account/
  - /articles/upgrading-your-personal-account-from-free-to-paid-with-a-credit-card/
  - /articles/upgrading-your-personal-account-from-free-to-paid-with-paypal/
  - /articles/500-error-while-upgrading/
  - /articles/upgrading-your-organization-s-billing-plan/
  - /articles/changing-your-organization-billing-plan/
  - /articles/upgrading-your-organization-account-from-free-to-paid-with-a-credit-card/
  - /articles/upgrading-your-organization-account-from-free-to-paid-with-paypal/
  - /articles/upgrading-your-organization-account/
  - /articles/switching-from-per-repository-to-per-user-pricing/
  - /articles/adding-seats-to-your-organization/
  - /articles/upgrading-your-github-billing-plan/
  - /articles/upgrading-your-github-subscription
  - /github/setting-up-and-managing-billing-and-payments-on-github/managing-billing-for-your-github-account/upgrading-your-github-subscription
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Organizations
  - Troubleshooting
  - Upgrades
  - User account
shortTitle: Upgrade your subscription
---

## Abonnement Deines persönlichen Kontos heraufstufen

Du kannst Dein persönliches Konto von {% data variables.product.prodname_free_user %} auf {% data variables.product.prodname_pro %} heraufstufen, um erweiterte Code-Review-Werkzeuge für private Repositorys zu erhalten. {% data reusables.gated-features.more-info %}

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.billing_plans %}
1. Next to "Current plan", click **Upgrade**. ![Schaltfläche „Upgrade“](/assets/images/help/billing/settings_billing_user_upgrade.png)
2. Under "Pro" on the "Compare plans" page, click **Upgrade to Pro**.
{% data reusables.dotcom_billing.choose-monthly-or-yearly-billing %}
{% data reusables.dotcom_billing.show-plan-details %}
{% data reusables.dotcom_billing.enter-billing-info %}
{% data reusables.dotcom_billing.enter-payment-info %}
{% data reusables.dotcom_billing.finish_upgrade %}

## Abonnement Deiner Organisation heraufstufen

Du kannst Deine Organisation von {% data variables.product.prodname_free_team %} für eine Organisation auf {% data variables.product.prodname_team %} heraufstufen, um auf erweiterte Werkzeuge für Zusammenarbeit und Management für Teams zuzugreifen, oder Dein Unternehmen auf {% data variables.product.prodname_ghe_cloud %} heraufstufen für zusätzliche Sicherheits-, Compliance- und Bereitstellungskontrollen. {% data reusables.gated-features.more-info-org-products %}

{% data reusables.dotcom_billing.org-billing-perms %}

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.upgrade_org %}
{% data reusables.dotcom_billing.choose_org_plan %}
{% data reusables.dotcom_billing.choose-monthly-or-yearly-billing %}
{% data reusables.dotcom_billing.show-plan-details %}
{% data reusables.dotcom_billing.enter-payment-info %}
{% data reusables.dotcom_billing.owned_by_business %}
{% data reusables.dotcom_billing.finish_upgrade %}

### Nächste Schritte für Organisationen mit {% data variables.product.prodname_ghe_cloud %}

Nach dem Heraufstufen Deiner Organisation auf {% data variables.product.prodname_ghe_cloud %} kannst Du die Identitäts- und Zugriffsverwaltung für Deine Organisation einrichten. Weitere Informationen finden Sie unter „[SAML Single Sign-On für Ihre Organisation verwalten](/organizations/managing-saml-single-sign-on-for-your-organization)“.

Wenn Du ein Enterprise-Konto mit {% data variables.product.prodname_ghe_cloud %} benutzen möchtest, kontaktiere bitte {% data variables.contact.contact_enterprise_sales %}. For more information, see "[About enterprise accounts](/enterprise-cloud@latest/admin/overview/about-enterprise-accounts){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation.{% else %}."{% endif %}

## Benutzer zu Deiner Organisation hinzufügen

Wenn Du zusätzlichen Benutzern den Zugriff auf die privaten Repositorys Deiner {% data variables.product.prodname_team %}-Organisation geben möchtest, kannst Du jederzeit zusätzliche Benutzer erwerben.

{% data reusables.organizations.billing-settings %}
{% data reusables.dotcom_billing.add-seats %}
{% data reusables.dotcom_billing.number-of-seats %}
{% data reusables.dotcom_billing.confirm-add-seats %}

## Deine Organisation von der Repository-abhängigen auf die benutzerabhängige Preisgestaltung umstellen

{% data reusables.dotcom_billing.switch-legacy-billing %} Weitere Informationen findest Du unter „[Über benutzerabhängige Preise](/articles/about-per-user-pricing)."

{% data reusables.organizations.billing-settings %}
5. Benutze rechts neben dem Plannamen das Dropdowmenü **Edit** (Bearbeiten) und wähle **Edit plan** (Plan bearbeiten). ![Dropdownmenü „Edit" (Bearbeiten)](/assets/images/help/billing/per-user-upgrade-button.png)
6. Klicke rechts von „Advanced tools for teams" (Erweiterte Werkzeuge für Teams) auf **Upgrade now** (jetzt heraufstufen). ![Schaltfläche „Upgrade now" (jetzt heraufstufen)](/assets/images/help/billing/per-user-upgrade-now-button.png)
{% data reusables.dotcom_billing.choose_org_plan %}
{% data reusables.dotcom_billing.choose-monthly-or-yearly-billing %}
{% data reusables.dotcom_billing.owned_by_business %}
{% data reusables.dotcom_billing.finish_upgrade %}

## Fehlerbehebung eines 500er-Fehlers beim Heraufstufen

{% data reusables.dotcom_billing.500-error %}

## Weiterführende Informationen

- „[Produkte von {% data variables.product.prodname_dotcom %}](/articles/github-s-products)“
- „[Wie wirkt sich das Herauf- oder Herabstufen auf den Abrechnungsprozess aus?](/articles/how-does-upgrading-or-downgrading-affect-the-billing-process)“
- „[Informationen zur Abrechnung auf {% data variables.product.prodname_dotcom %}](/articles/about-billing-on-github).“
