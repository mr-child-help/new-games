---
title: GitHub Sponsors für Deine Organisation einrichten
intro: 'Deine Organisation kann {% data variables.product.prodname_sponsors %} beitreten, um Zahlungen für Eure Arbeit zu erhalten.'
redirect_from:
  - /articles/setting-up-github-sponsorship-for-your-organization
  - /articles/receiving-sponsorships-as-a-sponsored-organization
  - /github/supporting-the-open-source-community-with-github-sponsors/setting-up-github-sponsors-for-your-organization
permissions: 'Organization owners can set up {% data variables.product.prodname_sponsors %} for an organization.'
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Organizations
  - Sponsors profile
  - Open Source
shortTitle: Set up for organization
---

## {% data variables.product.prodname_sponsors %} beitreten

{% data reusables.sponsors.you-can-be-a-sponsored-organization %} {% data reusables.sponsors.stripe-supported-regions %}

Nachdem Du für Deine Organisation einen Einladung erhalten hast, um {% data variables.product.prodname_sponsors %} beizutreten, kannst du die unten stehenden Schritte abschließen, um eine unterstützte Organisation zu werden.

Um {% data variables.product.prodname_sponsors %} als ein einzelner Mitwirkender außerhalb einer Organisation beizutreten, siehe „[{% data variables.product.prodname_sponsors %} für Dein Benutzerkonto einrichten](/sponsors/receiving-sponsorships-through-github-sponsors/setting-up-github-sponsors-for-your-user-account)."

{% data reusables.sponsors.navigate-to-github-sponsors %}
{% data reusables.sponsors.view-eligible-accounts %}
3. Klicke rechts neben Deiner Organisation auf **Join the waitlist** (Der Warteliste beitreten).
{% data reusables.sponsors.contact-info %}
{% data reusables.sponsors.accept-legal-terms %}

## Dein Profil als unterstützte Organisation vervollständigen

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.navigate-to-profile-tab %}
{% data reusables.sponsors.short-bio %}
{% data reusables.sponsors.add-introduction %}
{% data reusables.sponsors.meet-the-team %}
{% data reusables.sponsors.edit-featured-work %}
{% data reusables.sponsors.opt-in-to-being-featured %}
{% data reusables.sponsors.save-profile %}

## Sponsoring-Stufen erstellen

{% data reusables.sponsors.tier-details %}

{% data reusables.sponsors.maximum-tier %}

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.navigate-to-sponsor-tiers-tab %}
{% data reusables.sponsors.click-add-tier %}
{% data reusables.sponsors.tier-price-description %}
{% data reusables.sponsors.add-welcome-message %}
{% data reusables.sponsors.save-tier-draft %}
{% data reusables.sponsors.review-and-publish-tier %}
{% data reusables.sponsors.add-more-tiers %}

## Deine Bankinformationen einreichen

As a sponsored organization, you will receive payouts to a bank account in a supported region. This can be a dedicated bank account for your organization or a personal bank account. You can get a business bank account through services like [Stripe Atlas](https://stripe.com/atlas) or join a fiscal host like [Open Collective](https://opencollective.com/). The person setting up {% data variables.product.prodname_sponsors %} for the organization must live in the same supported region, too. {% data reusables.sponsors.stripe-supported-regions %}

{% data reusables.sponsors.double-check-stripe-info %}

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.create-stripe-account %}

For more information about setting up Stripe Connect using Open Collective, see [Setting up {% data variables.product.prodname_sponsors %}](https://docs.opencollective.com/help/collectives/github-sponsors) in the Open Collective Docs.

## Deine Steuerinformationen einreichen

{% data reusables.sponsors.tax-form-information-org %}

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.settings-tab %}
{% data reusables.sponsors.country-of-residence %}
{% data reusables.sponsors.overview-tab %}
{% data reusables.sponsors.tax-form-link %}

## Zwei-Faktor-Authentifizierung (2FA) für Dein {% data variables.product.prodname_dotcom %}-Konto aktivieren

Before your organization can become a sponsored organization, you must enable 2FA for your account on {% data variables.product.product_location %}. Weitere Informationen finden Sie unter „[Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication)“.

## Deinen Antrag bei {% data variables.product.prodname_dotcom %} zur Genehmigung einreichen

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.request-approval %}

{% data reusables.sponsors.github-review-app %}

## Weiterführende Informationen
- „[Informationen zu {% data variables.product.prodname_sponsors %}](/sponsors/getting-started-with-github-sponsors/about-github-sponsors)“
- "[Receiving sponsorships through {% data variables.product.prodname_sponsors %}](/sponsors/receiving-sponsorships-through-github-sponsors)"
