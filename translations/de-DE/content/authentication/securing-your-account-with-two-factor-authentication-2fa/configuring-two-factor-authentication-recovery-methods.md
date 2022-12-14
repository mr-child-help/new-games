---
title: Wiederherstellungsmethoden bei der Zwei-Faktor-Authentifizierung konfigurieren
intro: 'Du kannst verschiedene Wiederherstellungsmethoden einrichten, um auf Dein Konto zuzugreifen, wenn Du Deine Anmeldeinformation für die Zwei-Faktor-Authentifizierung verloren hast.'
redirect_from:
  - /articles/downloading-your-two-factor-authentication-recovery-codes/
  - /articles/setting-a-fallback-authentication-number/
  - /articles/about-recover-accounts-elsewhere/
  - /articles/adding-a-fallback-authentication-method-with-recover-accounts-elsewhere/
  - /articles/generating-and-storing-an-account-recovery-token/
  - /articles/configuring-two-factor-authentication-recovery-methods
  - /github/authenticating-to-github/configuring-two-factor-authentication-recovery-methods
  - /github/authenticating-to-github/securing-your-account-with-two-factor-authentication-2fa/configuring-two-factor-authentication-recovery-methods
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - 2FA
shortTitle: Configure 2FA recovery
---

Neben der sicheren Speicherung Deiner Wiederherstellungscodes für die Zwei-Faktor-Authentifizierung (2FA) empfehlen wir außerdem dringend, mindestens eine zusätzliche Wiederherstellungsmethode zu konfigurieren.

## Wiederherstellungscode für die Zwei-Faktor-Authentifizierung herunterladen

{% data reusables.two_fa.about-recovery-codes %} Sie können nach der Aktivierung der Zwei-Faktor-Authentifizierung Ihre Wiederherstellungscodes auch jederzeit herunterladen.

Um Dein Konto zu schützen, solltest Du diese Wiederherstellungscode nicht öffentlich machen und nicht weitergeben. Wir empfehlen, die Codes mit einem sicheren Passwort-Manager zu speichern, beispielsweise mit:
- [1Password](https://1password.com/)
- [LastPass](https://lastpass.com/)

Wenn Du neue Wiederherstellungscodes erzeugst oder die 2FA deaktivierst und erneut aktivierst, werden die Wiederherstellungscodes in Deinen Sicherheitseinstellungen automatisch aktualisiert.

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.security %}
{% data reusables.two_fa.show-recovery-codes %}
4. Speichere Deine Wiederherstellungscodes an einem sicheren Ort. Mit Deinen Wiederherstellungscodes kannst Du wieder auf Dein Konto zugreifen, wenn Du den Zugriff darauf verlierst.
    - Um Ihre Wiederherstellungscodes auf Ihrem Gerät zu speichern, klicken Sie auf **Download** (Herunterladen).
    - Um eine physische Kopie Ihrer Wiederherstellungscodes aufzubewahren, klicken Sie auf **Print** (Drucken).
    - Um Ihre Wiederherstellungscodes zur Speicherung in einem Passwort-Manager zu kopieren, klicken Sie auf **Copy** (Kopieren). ![Liste der Wiederherstellungscodes mit Option zum Herunterladen, Drucken oder Kopieren der Codes](/assets/images/help/2fa/download-print-or-copy-recovery-codes-before-continuing.png)

## Einen neuen Satz an Wiederherstellungscodes erzeugen

Wenn Du einen Wiederherstellungscode genutzt hast, um wieder Zugriff auf Dein Konto zu erhalten, kannst Du diesen Code nicht mehr verwenden. Wenn Du alle 16 Wiederherstellungscodes aufgebraucht hast, kannst Du eine neue Liste mit Codes erzeugen. Durch das Erstellen einer neuen Liste mit Wiederherstellungscodes werden alle zuvor erzeugten Codes ungültig.

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.security %}
{% data reusables.two_fa.show-recovery-codes %}
3. Um einen weiteren Satz an Wiederherstellungscodes zu erstellen, klicke auf **Generate new recovery codes** (Neue Wiederherstellungscodes erzeugen). ![Schaltfläche „Generate new recovery codes“ (Neue Wiederherstellungscodes erzeugen)](/assets/images/help/2fa/generate-new-recovery-codes.png)

## Einen Sicherheitsschlüssel als zusätzliche Methode für die Zwei-Faktor-Authentifizierung konfigurieren

Du kannst einen Sicherheitsschlüssel als sekundäre Zwei-Faktor-Authentifizierungsmethode festlegen und diesen Schlüssel nutzen, um erneut Zugriff auf Dein Konto zu erhalten. Weitere Informationen finden Sie unter „[Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication#configuring-two-factor-authentication-using-a-security-key)“.

{% ifversion fpt or ghec %}

## Eine Fallback-Authentifizierungsnummer festlegen

Du kannst eine zweite Nummer für ein Fallback-Gerät angeben. Wenn Du weder auf Dein primäres Gerät noch auf Deine Wiederherstellungscodes zugreifen kannst, ermöglicht eine Ersatztelefonnummer für SMS den erneuten Zugriff auf Dein Konto.

Du kannst eine Fallback-Nummer unabhängig davon verwenden, ob Du die Authentifizierung per SMS oder TOTP-Mobilanwendung konfiguriert hast.

{% warning %}

**Warnung:** Die Verwendung einer Fallback-Nummer ist die letzte Option. Wir empfehlen, zusätzliche Wiederherstellungsmethoden zu konfigurieren, wenn Du eine Fallback-Authentifizierungsnummer festlegst.
- Die Authentifizierung über SMS ist riskant, da Mobilfunkanbieter angreifbar sind.
- SMS-Nachrichten werden nur für bestimmte Länder außerhalb der USA unterstützt. Die entsprechende Liste findest Du unter „[Länder, in denen die SMS-Authentifizierung unterstützt wird](/articles/countries-where-sms-authentication-is-supported)“.

{% endwarning %}

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.security %}
3. Klicke neben „Fallback SMS number“ (Fallback-SMS-Nummer) auf **Add** (Hinzufügen). ![Schaltfläche „Add fallback SMS number“ (Hinzufügen einer Fallback-SMS-Nummer)](/assets/images/help/2fa/add-fallback-sms-number-button.png)
4. Klicke unter „Fallback SMS number“ auf **Add fallback SMS number** (Fallback-SMS-Nummer hinzufügen). ![Text „Add fallback SMS number“ (Fallback-SMS-Nummer hinzufügen)](/assets/images/help/2fa/add_fallback_sms_number_text.png)
5. Wählen Sie Ihre Landesvorwahl aus, und geben Sie Ihre komplette Mobiltelefonnummer ein. Wenn Deine Angaben korrekt sind, klicke auf **Set fallback** (Fallback festlegen). ![Fallback-SMS-Nummer festlegen](/assets/images/help/2fa/2fa-fallback-number.png)

Nach der Einrichtung wird eine Bestätigungs-SMS an Dein Backup-Gerät gesendet.

{% endif %}

## Weiterführende Informationen

- „[Informationen zur Zwei-Faktor-Authentifizierung](/articles/about-two-factor-authentication)“
- „[Zwei-Faktor-Authentifizierung konfigurieren](/articles/configuring-two-factor-authentication)“
- „[Mit Zwei-Faktor-Authentifizierung auf {% data variables.product.prodname_dotcom %} zugreifen](/articles/accessing-github-using-two-factor-authentication)“
- „[Ihr Konto beim Verlust der Anmeldeinformationen für die Zwei-Faktor-Authentifizierung wiederherstellen](/articles/recovering-your-account-if-you-lose-your-2fa-credentials)“
