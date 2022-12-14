---
title: Zugriff auf Deine Organisation bei nicht verfügbarem Identitätsanbieter
intro: 'Administratoren von Organisationen können sich bei {% data variables.product.product_name %} anmelden, auch wenn ihr Identitätsanbieter nicht verfügbar ist, indem sie Single Sign-On umgehen und ihre Wiederherstellungscodes verwenden.'
product: '{% data reusables.gated-features.saml-sso %}'
redirect_from:
  - /articles/accessing-your-organization-if-your-identity-provider-is-unavailable
  - /github/setting-up-and-managing-organizations-and-teams/accessing-your-organization-if-your-identity-provider-is-unavailable
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Unavailable identity provider
---

Administratoren von Organisationen können [einen ihrer heruntergeladenen oder gespeicherten Wiederherstellungscodes](/articles/downloading-your-organization-s-saml-single-sign-on-recovery-codes) verwenden, um Single-Sign-On zu umgehen. You may have saved these to a password manager, such as [LastPass](https://lastpass.com/) or [1Password](https://1password.com/).

{% note %}

**Hinweis:** Du kannst Wiederherstellungscodes nur einmal und in aufeinanderfolgender Reihenfolge verwenden. Wiederherstellungscodes gewähren den Zugriff für 24 Stunden.

{% endnote %}

1. Klicke unten im Single Sign-On-Dialog auf **Use a recovery code** (Wiederherstellungscode verwenden), um Single Sign-On zu umgehen. ![Link zum Eingeben Deines Wiederherstellungscodes](/assets/images/help/saml/saml_use_recovery_code.png)
2. Gib im Feld „Recovery Code“ (Wiederherstellungscode) Deinen Wiederherstellungscode ein. ![Feld zum Eingeben Deines Wiederherstellungscodes](/assets/images/help/saml/saml_recovery_code_entry.png)
3. Klicke auf **Verify** (Bestätigen). ![Schaltfläche zum Bestätigen Deines Wiederherstellungscodes](/assets/images/help/saml/saml_verify_recovery_codes.png)

Denke daran, dass ein Wiederherstellungscode nicht mehr gültig ist, nachdem Du ihn verwendet hast. Du kannst den Wiederherstellungscode nicht erneut verwenden.

## Weiterführende Informationen

- „[Informationen zum Identitäts- und Zugriffsmanagement mit SAML SSO](/articles/about-identity-and-access-management-with-saml-single-sign-on)“
