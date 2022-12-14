---
title: Informationen zur Zwei-Faktor-Authentifizierung und zu SAML Single-Sign-On
intro: 'Administratoren von Organisationen können sowohl SAML Single-Sign-On als auch die Zwei-Faktor-Authentifizierung aktivieren, um zusätzliche Authentifizierungsmaßnahmen für ihre Organisationsmitglieder hinzuzufügen.'
product: '{% data reusables.gated-features.saml-sso %}'
redirect_from:
  - /articles/about-two-factor-authentication-and-saml-single-sign-on
  - /github/setting-up-and-managing-organizations-and-teams/about-two-factor-authentication-and-saml-single-sign-on
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: 2FA & SAML single sign-on
---

Die Zwei-Faktor-Authentifizierung (2FA) bietet die grundlegende Authentifizierung für Organisationsmitglieder. By enabling 2FA, organization administrators limit the likelihood that a member's account on {% data variables.product.product_location %} could be compromised. Weitere Informationen zur Zwei-Faktor-Authentifizierung findest Du unter „[Informationen zur Zwei-Faktor-Authentifizierung](/articles/about-two-factor-authentication).“

Um zusätzliche Authentifizierungsmaßnahmen hinzuzufügen, können Organisationsadministratoren außerdem [SAML Single-Sign-On (SSO) aktivieren](/articles/enabling-and-testing-saml-single-sign-on-for-your-organization), sodass Organisationsmitglieder Single-Sign-On für den Zugriff auf eine Organisation verwenden müssen. Weitere Informationen zu SAML SSO findest Du unter „[Informationen zum Identitäts- und Zugriffsmanagement mit SAML Single Sign-On](/articles/about-identity-and-access-management-with-saml-single-sign-on).“

Wenn sowohl die Zwei-Faktor-Authentifizierung als auch SAML SSO aktiviert sind, müssen Organisationsmitglieder wie folgt vorgehen:
- Use 2FA to log in to their account on {% data variables.product.product_location %}
- Mit Single Sign-On auf die Organisation zugreifen
- Ein autorisiertes Token für den API- oder Git-Zugriff verwenden und Single-Sign-On zur Autorisierung des Tokens verwenden

## Weiterführende Informationen

- „[SAML Single Sign-On für Deine Organisation erzwingen](/articles/enforcing-saml-single-sign-on-for-your-organization)“
