---
title: Issues deaktivieren
intro: 'Du kannst Issues für Dein Repository deaktivieren, wenn Du keine Beiträge oder Fehlerberichte akzeptierst.'
redirect_from:
  - /github/managing-your-work-on-github/managing-your-work-with-issues-and-pull-requests/disabling-issues
  - /articles/disabling-issues
  - /github/managing-your-work-on-github/disabling-issues
  - /github/administering-a-repository/managing-repository-settings/disabling-issues
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
3. Hebe unter „Features“ (Funktionen) die Auswahl des Kontrollkästchens **Issues** (Issues) auf. ![Kontrollkästchen „Remove Issues" (Entfernen von Issues)](/assets/images/help/issues/issues_settings_remove_from_repo.png)

Wenn Du Issues zukünftig erneut aktivieren möchtest, sind alle Issues wieder verfügbar, die zuvor hinzugefügt wurden.

{% ifversion fpt or ghec %}

{% tip %}

Wende Dich an {% data variables.contact.contact_support %}, wenn Du Issues wegen missbräuchlicher Verwendung durch Fremde deaktivieren möchtest.
{% data reusables.policies.abuse %}

{% endtip %}

{% endif %}
