---
title: Anmeldeinformationen für den Zugriff auf GitHub aktualisieren
intro: '{% data variables.product.product_name %} credentials include{% ifversion not ghae %} not only your password, but also{% endif %} the access tokens, SSH keys, and application API tokens you use to communicate with {% data variables.product.product_name %}. Bei Bedarf kannst Du alle diese Anmeldeinformationen selber zurücksetzen.'
redirect_from:
  - /articles/rolling-your-credentials/
  - /articles/how-can-i-reset-my-password/
  - /articles/updating-your-github-access-credentials
  - /github/authenticating-to-github/updating-your-github-access-credentials
  - /github/authenticating-to-github/keeping-your-account-and-data-secure/updating-your-github-access-credentials
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Update access credentials
---

{% ifversion not ghae %}
## Neues Passwort anfordern

1. To request a new password, visit {% ifversion fpt or ghec %}https://{% data variables.product.product_url %}/password_reset{% else %}`https://{% data variables.product.product_url %}/password_reset`{% endif %}.
2. Enter the email address associated with your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}, then click **Send password reset email.** The email will be sent to the backup email address if you have one configured. ![Dialogfeld zum Anfordern einer E-Mail für die Passwortzurücksetzung](/assets/images/help/settings/password-recovery-email-request.png)
3. Die E-Mail enthält einen Link, über den Du Dein Passwort zurücksetzen kannst. Auf diesen Link musst Du innerhalb von drei Stunden nach Erhalt der E-Mail klicken. Falls Du keine E-Mail von uns erhalten hast, siehe in Deinem Spam-Ordner nach.
4. If you have enabled two-factor authentication, you will be prompted for your 2FA credentials. Type your 2FA credentials or one of your 2FA recovery codes and click **Verify**. ![Two-factor authentication prompt](/assets/images/help/2fa/2fa-password-reset.png)
5. Type a new password, confirm your new password, and click **Change password**. For help creating a strong password, see "[Creating a strong password](/articles/creating-a-strong-password)."
  {% ifversion fpt or ghec %}![Password recovery box](/assets/images/help/settings/password-recovery-page.png){% else %}
  ![Feld für Passwortwiederherstellung](/assets/images/enterprise/settings/password-recovery-page.png){% endif %}

{% tip %}

To avoid losing your password in the future, we suggest using a secure password manager, like [LastPass](https://lastpass.com/) or [1Password](https://1password.com/).

{% endtip %}

## Vorhandenes Passwort ändern

{% data reusables.repositories.blocked-passwords %}

1. {% data variables.product.signin_link %} für {% data variables.product.product_name %}.
{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.security %}
4. Gib unter „Change password“ (Passwort ändern) Dein altes Passwort und ein sicheres neues Passwort ein, und bestätige das neue Passwort. Details zur Erstellung eines sicheren Passworts findest Du unter „[Sicheres Passwort erstellen](/articles/creating-a-strong-password).“
5. Klicke auf **Update password** (Passwort aktualisieren).

{% tip %}

Für noch mehr Sicherheit empfehlen wir Dir zusätzlich zur Änderung Deines Passworts die Aktivierung der Zwei-Faktor-Authentifizierung. Details findest Du unter „[Informationen zur Zwei-Faktor-Authentifizierung](/articles/about-two-factor-authentication)“.

{% endtip %}
{% endif %}
## Zugriffstoken aktualisieren

Anweisungen zum Überprüfen und Löschen Deiner Zugriffstokens findest Du unter „[Deine autorisierten Integrationen überprüfen](/articles/reviewing-your-authorized-integrations)“. To generate new access tokens, see "[Creating a personal access token](/github/authenticating-to-github/creating-a-personal-access-token)."

## SSH-Schlüssel aktualisieren

Anweisungen zum Überprüfen und Löschen von SSH-Schlüsseln findest Du unter „[Deine SSH-Schlüssel überprüfen](/articles/reviewing-your-ssh-keys)“. Informationen zum Generieren und Hinzufügen neuer SSH-Schlüssel findest Du unter „[SSH-Schlüssel generieren](/articles/generating-an-ssh-key).“

## API-Token zurücksetzen

Wenn Sie bei {% data variables.product.product_name %} Anwendungen registriert haben, müssen Sie eventuell OAuth-Token zurücksetzen. For more information, see the "[Reset an authorization](/rest/reference/apps#reset-an-authorization)" endpoint.

{% ifversion not ghae %}
## Nicht autorisierten Zugriff verhindern

Weitere Empfehlungen zum Schutz Deines Kontos und zur Verhinderung von nicht autorisierten Zugriffen findest Du unter „[Nicht autorisierten Zugriff verhindern](/articles/preventing-unauthorized-access).“
{% endif %}
