---
title: Ein sicheres Passwort erstellen
intro: 'Secure your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %} with a strong and unique password using a password manager.'
redirect_from:
  - /articles/what-is-a-strong-password/
  - /articles/creating-a-strong-password
  - /github/authenticating-to-github/creating-a-strong-password
  - /github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-strong-password
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Create a strong password
---

You must choose or generate a password for your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %} that is at least:
- {% ifversion ghes %}Seven{% else %}Eight{% endif %} characters long, if it includes a number and a lowercase letter, or
- 15 Zeichen lang ist, bei einer beliebigen Kombination an Zeichen.

Für den Schutz Deines Kontos empfehlen wir Dir die folgenden Best Practices:
- Use a password manager, such as [LastPass](https://lastpass.com/) or [1Password](https://1password.com/), to generate a password of at least 15 characters.
- Erzeugen Sie ein eindeutiges Passwort für {% data variables.product.product_name %}. If you use your {% data variables.product.product_name %} password elsewhere and that service is compromised, then attackers or other malicious actors could use that information to access your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}.

- Konfiguriere die Zwei-Faktor-Authentifizierung für Dein persönliches Konto. Weitere Informationen findest Du unter „[Informationen zur Zwei-Faktor-Authentifizierung](/articles/about-two-factor-authentication).“
- Gib Dein Passwort niemals an andere weiter, auch nicht an potenzielle Mitarbeiter. Jede Person sollte ihr eigenes persönliches Konto bei {% data variables.product.product_name %} nutzen. Weitere Informationen zu Möglichkeiten der Zusammenarbeit findest Du unter „[Mitarbeiter in ein persönliches Repository einladen](/articles/inviting-collaborators-to-a-personal-repository)“, „[Informationen über gemeinschaftliche Entwicklungsmodelle](/articles/about-collaborative-development-models/)“ oder „[Mit Gruppen in Organisationen zusammenarbeiten](/organizations/collaborating-with-groups-in-organizations/).“

{% data reusables.repositories.blocked-passwords %}

You can only use your password to log on to {% data variables.product.product_name %} using your browser. When you authenticate to {% data variables.product.product_name %} with other means, such as the command line or API, you should use other credentials. For more information, see "[About authentication to {% data variables.product.prodname_dotcom %}](/github/authenticating-to-github/about-authentication-to-github)."

{% ifversion fpt or ghec %}{% data reusables.user_settings.password-authentication-deprecation %}{% endif %}

## Weiterführende Informationen

- "[Caching your {% data variables.product.product_name %} credentials in Git](/github/getting-started-with-github/caching-your-github-credentials-in-git/)"
- „[Dein Konto und Deine Daten schützen](/articles/keeping-your-account-and-data-secure/)“
