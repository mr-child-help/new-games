---
title: SSH-Verbindung testen
intro: 'After you''ve set up your SSH key and added it to your account on {% ifversion ghae %}{% data variables.product.product_name %}{% else %}{% data variables.product.product_location %}{% endif %}, you can test your connection.'
redirect_from:
  - /articles/testing-your-ssh-connection
  - /github/authenticating-to-github/testing-your-ssh-connection
  - /github/authenticating-to-github/connecting-to-github-with-ssh/testing-your-ssh-connection
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - SSH
shortTitle: Test your SSH connection
---

Vor dem Test Deiner SSH-Verbindung solltest Du:
- [nach vorhandenen SSH-Schlüsseln gesucht haben](/articles/checking-for-existing-ssh-keys)
- [neue SSH-Schlüssel generiert haben](/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
- [Deinem GitHub-Konto neue SSH-Schlüssel hinzugefügt haben](/articles/adding-a-new-ssh-key-to-your-github-account)

Für den Test Deiner Verbindung musst Du diese Aktion mit Deinem Passwort authentifizieren, welches der zuvor erstellten SSH-Schlüssel-Passphrase entspricht. Weitere Informationen zur Verwendung von SSH-Schlüssel-Passphrasen findest Du unter „[SSH-Schlüssel-Passphrasen verwenden](/articles/working-with-ssh-key-passphrases)“.

{% data reusables.command_line.open_the_multi_os_terminal %}
2. Gib den folgenden Befehl ein:
  ```shell
  $ ssh -T git@{% data variables.command_line.codeblock %}
  # versucht ssh zu {% data variables.product.product_name %}
  ```

  Eventuell erhälst Du eine Warnung wie die folgende:

  ```shell
  > The authenticity of host '{% data variables.command_line.codeblock %} (IP ADDRESS)' can't be established.
  > RSA key fingerprint is SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8.
  > Are you sure you want to continue connecting (yes/no)?
  ```

3. Verify that the fingerprint in the message you see matches {% ifversion fpt or ghec %}[{% data variables.product.prodname_dotcom %}'s RSA public key fingerprint](/github/authenticating-to-github/githubs-ssh-key-fingerprints){% else %} your enterprise's public key fingerprint{% endif %}. If it does, then type `yes`:
  ```shell
  > Hi <em>username</em>! You've successfully authenticated, but GitHub does not
  > provide shell access.
  ```

  {% linux %}

  Eventuell wird folgende Fehlermeldung angezeigt:
  ```shell
  ...
  Agent admitted failure to sign using the key.
  debug1: No more authentication methods to try.
  Permission denied (publickey).
  ```

  Dies ist ein bekanntes Problem einiger Linux-Distributionen. Weitere Informationen findest Du unter „[Fehler: Agent gibt Signierfehler zu](/articles/error-agent-admitted-failure-to-sign)“.

  {% endlinux %}

4. Vergewissere Dich, dass die resultierende Meldung Deinen Benutzernamen enthält. Wenn Du die Meldung „Permission denied“ (Berechtigung verweigert) erhältst, findest Du weitere Informationen unter „[Fehler: Berechtigung verweigert (publickey)](/articles/error-permission-denied-publickey)“.
