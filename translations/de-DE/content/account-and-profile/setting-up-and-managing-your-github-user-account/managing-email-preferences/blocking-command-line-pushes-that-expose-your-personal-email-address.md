---
title: 'Pushes über die Befehlszeile blockieren, die Deine private E-Mail-Adresse offenlegen'
intro: 'Wenn Du festgelegt hast, dass Deine E-Mail-Adresse beim Durchführen webbasierter Vorgänge nicht offengelegt wird, kannst Du auch Pushes über die Befehlszeile blockieren, die Deine private E-Mail-Adresse offenlegen könnten.'
redirect_from:
  - /articles/blocking-command-line-pushes-that-expose-your-personal-email-address
  - /github/setting-up-and-managing-your-github-user-account/blocking-command-line-pushes-that-expose-your-personal-email-address
  - /github/setting-up-and-managing-your-github-user-account/managing-email-preferences/blocking-command-line-pushes-that-expose-your-personal-email-address
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Accounts
  - Notifications
shortTitle: Block push with personal email
---

Wenn Du Commits über die Befehlszeile freigibst, wird die E-Mail-Adresse, die Du [in Git festgelegt](/articles/setting-your-commit-email-address) hast, mit Deinen Commits verknüpft. If you enable this setting, each time you push to GitHub, we’ll check the most recent commit. If the author email on that commit is a private email on your GitHub account, we will block the push and warn you about exposing your private email.

{% data reusables.user_settings.about-commit-email-addresses %}

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.emails %}
{% data reusables.user_settings.keeping_your_email_address_private %}
4. Um eine Offenlegung Deiner E-Mail-Adresse bei Commits, die Du über die Befehlszeile freigibst, zu verhindern, wähle **Block command line pushes that expose my email** (Pushes über die Befehlszeile blockieren, die meine E-Mail-Adresse offenlegen) aus. ![Option zum Blockieren von Befehlszeilen-Pushes, die E-Mail-Adressen offenlegen](/assets/images/help/settings/email_privacy_block_command_line_pushes.png)

## Weiterführende Informationen

- „[Commit-E-Mail-Adresse festlegen](/articles/setting-your-commit-email-address)“
