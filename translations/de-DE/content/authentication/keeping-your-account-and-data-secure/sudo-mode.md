---
title: Sudo-Modus
intro: '{% data variables.product.product_name %} fragt Sie nach Ihrem Passwort, wenn Sie Ihre E-Mail-Adresse ändern, Drittanbieteranwendungen autorisieren, neue öffentliche Schlüssel hinzufügen oder andere *durch Sudo geschützte* Aktionen ausführen möchten.'
redirect_from:
  - /articles/sudo-mode
  - /github/authenticating-to-github/sudo-mode
  - /github/authenticating-to-github/keeping-your-account-and-data-secure/sudo-mode
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
---

Nach der Ausführung einer durch sudo geschützten Aktion wirst Du erst nach mehreren Stunden der Inaktivität wieder zur Authentifizierung aufgefordert. Der Timer wird nach jeder durch sudo geschützten Aktion zurückgesetzt.

![Dialogfeld für den sudo-Modus](/assets/images/help/settings/sudo_mode_popup.png)

## Weiterführende Informationen

- [UNIX-Befehl `sudo`](http://en.wikipedia.org/wiki/Sudo)
