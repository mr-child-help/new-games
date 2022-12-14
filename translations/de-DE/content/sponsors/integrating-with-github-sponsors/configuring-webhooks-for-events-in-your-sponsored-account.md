---
title: Webhooks für Ereignisse in deinem unterstützten Konto konfigurieren
intro: 'Du kannst Webhooks konfigurieren, damit Du benachrichtigt wirst, wenn Du ein neues Sponsoring erhältst, oder wenn bestehende Sponsoren Änderungen an ihren Sponsorings machen.'
redirect_from:
  - /github/supporting-the-open-source-community-with-github-sponsors/configuring-webhooks-for-events-in-your-sponsored-account
versions:
  fpt: '*'
  ghec: '*'
type: how_to
topics:
  - Webhooks
  - Events
  - Open Source
shortTitle: Webhooks for events
---

## About webhooks for events in your sponsored account

Damit Du Änderungen wie zum Beispiel die Kündigung eines Sponsorings am Ende der Zahlungsperiode überwachen kannst, kannst Du Webhooks für Deine unterstützten Benutzer- oder Organisations-Konten erstellen. When you set up a webhook for your sponsored account, you'll receive updates when sponsorships are created, edited, or deleted. For more information, see the [`sponsorship` webhook event](/webhooks/event-payloads/#sponsorship).

## Managing webhooks for events in your sponsored account

{% data reusables.sponsors.navigate-to-sponsors-dashboard %}
{% data reusables.sponsors.navigate-to-webhooks-tab %}
{% data reusables.sponsors.add-webhook %}
{% data reusables.sponsors.add-payload-url %}
{% data reusables.sponsors.webhook-content-formatting %}
{% data reusables.sponsors.webhook-secret-token %}
{% data reusables.sponsors.add-active-triggers %}
{% data reusables.sponsors.confirm-add-webhook %}
{% data reusables.sponsors.manage-existing-webhooks %}
