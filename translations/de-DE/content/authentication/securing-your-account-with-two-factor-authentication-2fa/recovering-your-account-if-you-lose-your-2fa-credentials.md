---
title: Dein Konto beim Verlust der 2FA-Anmeldeinformationen wiederherstellen
intro: 'Wenn Du den Zugriff auf Deine Anmeldeinformationen für die Zwei-Faktor-Authentifizierung verlierst, kannst Du Deine Wiederherstellungscodes oder eine andere Wiederherstellungsoption verwenden, um wieder Zugriff auf Dein Konto zu erhalten.'
redirect_from:
  - /articles/recovering-your-account-if-you-lost-your-2fa-credentials/
  - /articles/authenticating-with-an-account-recovery-token/
  - /articles/recovering-your-account-if-you-lose-your-2fa-credentials
  - /github/authenticating-to-github/recovering-your-account-if-you-lose-your-2fa-credentials
  - /github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa/recovering-your-account-if-you-lose-your-2fa-credentials
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - 2FA
shortTitle: Recover an account with 2FA
---

{% ifversion fpt or ghec %}

{% warning %}

**Warnung:** {% data reusables.two_fa.support-may-not-help %}

{% endwarning %}

{% endif %}

## Einen Wiederherstellungscode für die Zwei-Faktor-Authentifizierung verwenden

Verwende einen Deiner Wiederherstellungscodes, um automatisch wieder Zugriff auf Dein Konto zu erhalten. Vielleicht hast Du Deine Wiederherstellungscodes in einem Passwort-Manager oder im Download-Ordner Deines Computers gespeichert. Der standardmäßige Dateiname für Wiederherstellungscodes lautet `github-recover-codes.txt`. Weitere Informationen zu Wiederherstellungscodes findest Du unter „[Wiederherstellungsmethoden bei der Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication-recovery-methods#downloading-your-two-factor-authentication-recovery-codes).“

{% data reusables.two_fa.username-password %}{% ifversion fpt or ghec %}
2. Klicke unter „Having Problems?" (Hast Du Probleme?) auf **Enter a two-factor recovery code** (Gib einen Zwei-Faktor-Wiederherstellungscode ein). ![Link to use a recovery code](/assets/images/help/2fa/2fa-recovery-code-link.png){% else %}
2. Klicke auf der 2FA-Seite unter „Don't have your phone?“ (Hast Du Dein Telefon nicht?) auf **Enter a two-factor recovery code** (Einen Zwei-Faktor-Wiederherstellungscode eingeben). ![Link to use a recovery code](/assets/images/help/2fa/2fa_recovery_dialog_box.png){% endif %}
3. Gib einen Deiner Wiederherstellungscodes ein, und klicke dann auf **Verify** (Verifizieren). ![Feld zum Eingeben eines Wiederherstellungscodes und Schaltfläche „Verify“ (Verifizieren)](/assets/images/help/2fa/2fa-type-verify-recovery-code.png)

{% ifversion fpt or ghec %}
## Authentifizierung mit einer Fallback-Nummer

Wenn Du Deine primäre TOTP-App oder Telefonnummer verlierst, kannst Du einen Zwei-Faktor-Authentifizierungscode eingeben, der an Deine Fallback-Nummer gesendet wurde, um automatisch wieder Zugriff auf Dein Konto zu erhalten.
{% endif %}

## Authentifizierung mit einem Sicherheitsschlüssel

Wenn Du die Zwei-Faktor-Authentifizierung mit einem Sicherheitsschlüssel konfiguriert hast, kannst Du den Sicherheitsschlüssel als sekundäre Authentifizierungsmethode verwenden, um automatisch wieder Zugriff auf Dein Konto zu erhalten. Weitere Informationen finden Sie unter „[Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)“.

{% ifversion fpt or ghec %}
## Authentifizierung mit einem verifizierten Gerät, einem SSH-Token oder einem persönlichen Zugriffstoken

If you know your {% data variables.product.product_name %} password but don't have the two-factor authentication credentials or your two-factor authentication recovery codes, you can have a one-time password sent to your verified email address to begin the verification process and regain access to your account.

{% note %}

**Hinweis**: Aus Sicherheitsgründen kann die Wiederherstellung des Zugriffs auf Dein Konto über die Authentifizierung mit einem einmal gültigen Passwort 3-5 Werktage dauern. Zusätzliche Anfragen, die während dieser Zeit eingereicht wurden, werden nicht überprüft.

{% endnote %}

Sie kannst die Anmeldeinformationen oder die Wiederherstellungscodes Deiner Zwei-Faktor-Authentifizierung verwenden, um jederzeit während der 3-5-tägigen Wartezeit den Zugriff auf Dein Konto wiederherzustellen.

1. Gib Deinen Benutzernamen und Dein Passwort ein, um die Authentifizierung durchzuführen. If you do not know your {% data variables.product.product_name %} password, you will not be able to generate a one-time password.
2. Klicke unter „Having Problems?" (Hast Du Probleme?) auf **Can't access your two factor device or valid recovery codes?** (Hast Du keinen Zugriff auf Dein Zwei-Faktor-Gerät oder auf gültige Wiederherstellungscodes?) ![Link, wenn Du Dein 2FA-Gerät oder Deine Wiederherstellungcodes nicht hast](/assets/images/help/2fa/no-access-link.png)
3. Klicke auf **I understand, get started** (Ich verstehe, lass uns beginnen), um ein Zurücksetzen Deiner Authentifizierungseinstellungen zu verlangen. ![Schaltfläche „Reset authentication settings" (Authentifizierungseinstellungen zurücksetzen)](/assets/images/help/2fa/reset-auth-settings.png)
4. Klicke auf **Send one-time password** (Sende ein einmal gültiges Passwort) um ein einmal gültiges Passwort an alle mit Deinem Konto verknüpften E-Mail-Adressen zu senden. ![Schaltfläche „Send one-time password" (Einmal gültiges Passwort senden)](/assets/images/help/2fa/send-one-time-password.png)
5. Gib unter „One-time password" (Einmal gültiges Passwort) das temporäre Passwort aus dem Wiederherstellungs-E-Mail von {% data variables.product.prodname_dotcom %} ein. ![Feld „One-time password" (Einmal gültiges Passwort)](/assets/images/help/2fa/one-time-password-field.png)
6. Klicke auf **Verify email address** (Verifiziere die E-Mail-Adresse).
7. Wähle einen alternativen Verifizierungsfaktor.
    - If you've used your current device to log into this account before and would like to use the device for verification, click **Verify with this device**.
    - Wenn Du bereits früher einen SSH-Schlüssel für dieses Konto eingerichtet hast und den SSH-Schlüssel zur Verifizierung verwenden möchtest, klicke auf **SSH key** (SSH-Schlüssel).
    - Wenn Du bereits früher ein persönliches Zugriffstoken eingerichtet hast und das persönliche Zugriffstoken zur Verifizierung verwenden möchtest, klicke auf **Personal access token** (Persönliches Zugriffstoken). ![Schaltfläche „Alternative verification" (Alternative Verifizierung)](/assets/images/help/2fa/alt-verifications.png)
8. Ein Mitarbeiter von {% data variables.contact.github_support %} wird Deine Anfrage prüfen und Dir innerhalb von 3-5 Werktagen eine E-Mail senden. Wenn Deine Anfrage genehmigt wurde, wirst Du einen Link erhalten, um Deinen Konto-Wiederherstellungsprozess abzuschließen. Wenn Deine Anfrage abgelehnt wurde, enthält die E-Mail eine Möglichkeit, den Support für alle weiteren Fragen zu kontaktieren.

## Authentifizierung mit einem Kontowiederherstellungstoken

{% warning %}

**Warning:** Account recovery tokens are deprecated and will be disabled on **December 1st, 2021**. Please ensure you have configured other two-factor recovery methods. For more information, see "[Configuring two-factor authentication recovery methods](/articles/configuring-two-factor-authentication-recovery-methods)."

{% endwarning %}

If you lose access to the two-factor authentication methods for your account on {% data variables.product.product_location %}, you can retrieve your account recovery token from a partner recovery provider and ask {% data variables.product.prodname_dotcom %} Support to review it.

Wenn Du keinen Zugriff auf Deine Zwei-Faktor-Authentifizierungsmethoden oder Wiederherstellungscodes hast und ein Kontowiederherstellungstoken mit „Recover Accounts Elsewhere" bei Facebook gespeichert hast, kannst Du möglicherweise mit diesem Token wieder Zugriff auf Dein Konto erlangen.

Wenn Du nicht in der Lage bist, den Zugang zu Deinem Konto wieder herzustellen, erstelle ein einmalig gültiges Passwort, um wieder Zugang zu erhalten. Weitere Informationen findest Du unter „[Authentifizierung mit einem verifizierten Gerät, einem SSH-Token oder einem persönlichen Zugriffstoken](#authenticating-with-a-verified-device-ssh-token-or-personal-access-token)."

{% warning %}

**Warnungen:**
- Bevor Du ein Kontowiederherstellungstoken abrufst, solltest Du versuchen, mit Deinen [Zwei-Faktor-Authentifizierungscodes](/articles/accessing-github-using-two-factor-authentication) oder Deinen Wiederherstellungscodes für die Zwei-Faktor-Authentifizierung wieder Zugriff auf Dein Konto zu erhalten. Weitere Informationen findest Du unter „[Dein Konto beim Verlust der 2FA-Anmeldeinformationen wiederherstellen](/articles/recovering-your-account-if-you-lose-your-2fa-credentials).“

{% endwarning %}

1. Rufe auf Facebook die Seite [Security Settings](https://www.facebook.com/settings?tab=security) (Sicherheitseinstellungen) auf, und klicke dann auf **Recover Accounts Elsewhere**. ![Facebook-Seite mit Sicherheitseinstellungen und Link zu „Recover Accounts Elsewhere"](/assets/images/help/settings/security-facebook-security-settings-page.png)
2. Click the recovery token associated with your account on {% data variables.product.product_location %}. ![Liste der auf Facebook gespeicherten Wiederherstellungstoken](/assets/images/help/settings/security-github-rae-token-on-facebook.png)
3. Um Dein Kontowiederherstellungstoken einzulösen, klicke auf **Recover This Account** (Dieses Konto wiederherstellen). Ein neues Fenster wird geöffnet, das Dich auf {% data variables.product.product_name %} zurückführt. ![Modales Feld mit Informationen zu Deinem Wiederherstellungstoken und Schaltfläche „Recover This Account“ (Dieses Konto wiederherstellen)](/assets/images/help/settings/security-recover-account-facebook.png)
4. Benachrichtige den {% data variables.contact.contact_support %}, dass Dein Kontowiederherstellungstoken bereit für den Review ist.
{% endif %}

## Weiterführende Informationen

- „[Informationen zur Zwei-Faktor-Authentifizierung](/articles/about-two-factor-authentication)“
- „[Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication)“
- „[Wiederherstellungsmethoden für die Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication-recovery-methods)“
- „[Mit Zwei-Faktor-Authentifizierung auf {% data variables.product.prodname_dotcom %} zugreifen](/articles/accessing-github-using-two-factor-authentication)“
