---
title: Deine primäre E-Mail-Adresse ändern
intro: Du kannst die mit Deinem Benutzerkonto verknüpfte E-Mail-Adresse jederzeit ändern.
redirect_from:
  - /articles/changing-your-primary-email-address
  - /github/setting-up-and-managing-your-github-user-account/changing-your-primary-email-address
  - /github/setting-up-and-managing-your-github-user-account/managing-email-preferences/changing-your-primary-email-address
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Accounts
  - Notifications
shortTitle: Primary email address
---

{% note %}

**Note:** You cannot change your primary email address to an email that is already set to be your backup email address.

{% endnote %}

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.emails %}
3. Wenn Du eine neue E-Mail-Adresse hinzufügen und als primäre E-Mail-Adresse festlegen möchtest, gib unter „Add email address“ (E-Mail-Adresse hinzufügen) eine neue E-Mail-Adresse ein. Klicke dann auf **Add** (Hinzufügen). ![Schaltfläche zum Hinzufügen einer anderen E-Mail-Adresse](/assets/images/help/settings/add_another_email_address.png)
4. Klicke im Dropdownmenü unter „Primary email address“ (Primäre E-Mail-Adresse) auf die E-Mail-Adresse, die Du als primäre E-Mail-Adresse festlegen möchtest, und klicke dann auf **Save** (Speichern). ![Schaltfläche zum Festlegen als primäre Adresse](/assets/images/help/settings/set_as_primary_email.png)
5. Um die alte E-Mail-Adresse aus Ihrem Konto zu entfernen, klicken Sie neben der alten E-Mail-Adresse auf {% octicon "trash" aria-label="The trash symbol" %}.
{% ifversion fpt or ghec %}
6. Verifiziere Deine neue primäre E-Mail-Adresse. Ohne verifizierte E-Mail-Adresse kannst Du nicht alle Funktionen von {% data variables.product.product_name %} nutzen. Weitere Informationen findest Du unter „[Eigene E-Mail-Adresse verifizieren](/articles/verifying-your-email-address).“
{% endif %}
