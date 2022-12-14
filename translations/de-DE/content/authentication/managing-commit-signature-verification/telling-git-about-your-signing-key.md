---
title: Git Deinen Signaturschlüssel mitteilen
intro: 'To sign commits locally, you need to inform Git that there''s a GPG or X.509 key you''d like to use.'
redirect_from:
  - /articles/telling-git-about-your-gpg-key/
  - /articles/telling-git-about-your-signing-key
  - /github/authenticating-to-github/telling-git-about-your-signing-key
  - /github/authenticating-to-github/managing-commit-signature-verification/telling-git-about-your-signing-key
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Identity
  - Access management
shortTitle: Tell Git your signing key
---

{% mac %}

## Git Deinen GPG-Schlüssel mitteilen

If you're using a GPG key that matches your committer identity and your verified email address associated with your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}, then you can begin signing commits and signing tags.

{% note %}

Wenn Du keinen GPG-Schlüssel hast, der Deiner Beitragender-Identität entspricht, musst Du Deinen Schlüssel mit einer E-Mail-Adresse verknüpfen. Weitere Informationen findest Du unter „[E-Mail-Adresse mit Deinem GPG-Schlüssel verknüpfen](/articles/associating-an-email-with-your-gpg-key)“.

{% endnote %}

Wenn Du mehrere GPG-Schlüssel hast, musst Du Git mitteilen, welcher zu verwenden ist.

{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.gpg.list-keys-with-note %}
{% data reusables.gpg.copy-gpg-key-id %}
{% data reusables.gpg.paste-gpg-key-id %}
1. If you aren't using the GPG suite, run the following command in the `zsh` shell to add the GPG key to your `.zshrc` file, if it exists, or your `.zprofile` file:
  ```shell
  $ if [ -r ~/.zshrc ]; then echo 'export GPG_TTY=$(tty)' >> ~/.zshrc; \
    else echo 'export GPG_TTY=$(tty)' >> ~/.zprofile; fi
  ```
  Alternatively, if you use the `bash` shell, run this command:
  ```shell
  $ if [ -r ~/.bash_profile ]; then echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile; \
    else echo 'export GPG_TTY=$(tty)' >> ~/.profile; fi
  ```

{% data reusables.gpg.x-509-key %}

{% endmac %}

{% windows %}

## Git Deinen GPG-Schlüssel mitteilen

If you're using a GPG key that matches your committer identity and your verified email address associated with your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}, then you can begin signing commits and signing tags.

{% note %}

Wenn Du keinen GPG-Schlüssel hast, der Deiner Beitragender-Identität entspricht, musst Du Deinen Schlüssel mit einer E-Mail-Adresse verknüpfen. Weitere Informationen findest Du unter „[E-Mail-Adresse mit Deinem GPG-Schlüssel verknüpfen](/articles/associating-an-email-with-your-gpg-key)“.

{% endnote %}

Wenn Du mehrere GPG-Schlüssel hast, musst Du Git mitteilen, welcher zu verwenden ist.

{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.gpg.list-keys-with-note %}
{% data reusables.gpg.copy-gpg-key-id %}
{% data reusables.gpg.paste-gpg-key-id %}

{% data reusables.gpg.x-509-key %}

{% endwindows %}

{% linux %}

## Git Deinen GPG-Schlüssel mitteilen

If you're using a GPG key that matches your committer identity and your verified email address associated with your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}, then you can begin signing commits and signing tags.

{% note %}

Wenn Du keinen GPG-Schlüssel hast, der Deiner Beitragender-Identität entspricht, musst Du Deinen Schlüssel mit einer E-Mail-Adresse verknüpfen. Weitere Informationen findest Du unter „[E-Mail-Adresse mit Deinem GPG-Schlüssel verknüpfen](/articles/associating-an-email-with-your-gpg-key)“.

{% endnote %}

Wenn Du mehrere GPG-Schlüssel hast, musst Du Git mitteilen, welcher zu verwenden ist.

{% data reusables.command_line.open_the_multi_os_terminal %}
{% data reusables.gpg.list-keys-with-note %}
{% data reusables.gpg.copy-gpg-key-id %}
{% data reusables.gpg.paste-gpg-key-id %}
1. To add your GPG key to your bash profile, run the following command:
  ```shell
  $ if [ -r ~/.bash_profile ]; then echo 'export GPG_TTY=$(tty)' >> ~/.bash_profile; \
    else echo 'export GPG_TTY=$(tty)' >> ~/.profile; fi
  ```
  {% note %}

  **Hinweis:** Wenn Du kein `.bash_profile` hast, fügt dieser Befehl Deinen GPG-Schlüssel zu `.profile` hinzu.

  {% endnote %}

{% endlinux %}

## Weiterführende Informationen

- „[Nach vorhandenen GPG-Schlüsseln suchen](/articles/checking-for-existing-gpg-keys)“
- „[Einen neuen GPG-Schlüssel erzeugen](/articles/generating-a-new-gpg-key)“
- „[Eine verifizierte E-Mail-Adresse in Deinem GPG-Schlüssel verwenden](/articles/using-a-verified-email-address-in-your-gpg-key)“
- „[Einen neuen GPG-Schlüssel zu Deinem GitHub-Konto hinzufügen](/articles/adding-a-new-gpg-key-to-your-github-account)“
- „[Eine E-Mail-Adresse mit Deinem GPG-Schlüssel verknüpfen](/articles/associating-an-email-with-your-gpg-key)“
- „[Commits signieren](/articles/signing-commits)“
- „[Tags signieren](/articles/signing-tags)“
