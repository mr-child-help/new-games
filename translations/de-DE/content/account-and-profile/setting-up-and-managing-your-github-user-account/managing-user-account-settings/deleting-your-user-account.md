---
title: Dein Benutzerkonto löschen
intro: 'Sie können Ihr {% data variables.product.product_name %}-Benutzerkonto jederzeit löschen.'
redirect_from:
  - /articles/deleting-a-user-account/
  - /articles/deleting-your-user-account
  - /github/setting-up-and-managing-your-github-user-account/deleting-your-user-account
  - /github/setting-up-and-managing-your-github-user-account/managing-user-account-settings/deleting-your-user-account
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
topics:
  - Accounts
shortTitle: Dein Benutzerkonto löschen
---

Wenn Du Dein Benutzerkonto löschst, werden alle dazugehörigen Repositorys, Forks von privaten Repositorys, Wikis, Issues, Pull Requests und Seiten Deines Kontos ebenfalls gelöscht. {% ifversion fpt or ghec %} Deine Issues, Pull Requests und Kommentare in Repositorys von anderen Benutzern werden nicht gelöscht, sondern mit unserem [Ghost user](https://github.com/ghost) (Geisterbenutzer) verknüpft.{% else %}Deine Issues, Pull Requests und Kommentare in Repositorys von anderen Benutzern werden nicht gelöscht.{% endif %}

{% ifversion fpt or ghec %} When you delete your account we stop billing you. The email address associated with the account becomes available for use with a different account on {% data variables.product.product_location %}. After 90 days, the account name also becomes available to anyone else to use on a new account. {% endif %}

Wenn Du der alleinige Inhaber einer Organisation bist, musst Du die Inhaberschaft auf eine andere Person übertragen oder die Organisation löschen, bevor Du Dein Benutzerkonto löschen kannst. Wenn es noch weitere Inhaber Deiner Organisation gibt, musst Du Dich selbst aus der Organisation löschen, bevor Du Dein Benutzerkonto löschen kannst.

Weitere Informationen findest Du unter:
- „[Inhaberschaft an einer Organisation übertragen](/articles/transferring-organization-ownership)“
- „[Ein Organisationskonto löschen](/articles/deleting-an-organization-account)“
- „[Dich selbst aus einer Organisation entfernen](/articles/removing-yourself-from-an-organization/)“

## Deine Kontoinformationen sichern

Bevor Du Dein Benutzerkonto löschst, erstelle Kopien aller Repositorys, privaten Forks, Wikis, Issues und Pull Requests Deines Kontos.

{% warning %}

**Warnung:** Sobald Dein Benutzerkonto gelöscht wurde, kann GitHub Deine Inhalte nicht wiederherstellen.

{% endwarning %}

## Dein Benutzerkonto löschen

{% data reusables.user_settings.access_settings %}
{% data reusables.user_settings.account_settings %}
3. Klicke unten auf der Seite mit den Kontoeinstellungen unter „Delete account“ (Konto löschen) auf **Delete your account** (Dein Konto löschen). Vor dem Löschen Deines Benutzerkontos musst Du Folgendes tun:
    - Wenn Du der alleinige Inhaber einer Organisation bist, musst Du die Inhaberschaft auf eine andere Person übertragen oder die Organisation löschen.
    - Wenn es andere Inhaber der Organisation gibt, musst Du Dich selbst aus der Organisation entfernen. ![Schaltfläche zum Löschen des Kontos](/assets/images/help/settings/settings-account-delete.png)
4. Fülle das Dialogfeld „Are you sure you want to do this?“ (Möchtest Du das wirklich tun?) aus, um zu bestätigen, dass Du die Folgen der Kontolöschung verstanden hast: ![Dialogfeld zum Bestätigen der Kontolöschung](/assets/images/help/settings/settings-account-deleteconfirm.png)
  {% ifversion fpt or ghec %}– Denken Sie daran, dass alle Repositorys, Forks von privaten Repositorys, Wikis, Issues, Pull Requests und Seiten von Ihrem Konto ebenfalls gelöscht werden, dass Ihre Abrechnung beendet wird und Ihr Benutzername wieder für die Verwendung auf {% data variables.product.product_name %} freigegeben wird.
  {% else %}– Denke daran, dass alle Repositorys, Forks von privaten Repositorys, Wikis, Issues, Pull Requests und Seiten von Deinem Konto ebenfalls gelöscht werden und Dein Benutzername wieder für die Verwendung auf {% data variables.product.product_name %} freigegeben wird.
  {% endif %}– Gib im ersten Feld Deinen {% data variables.product.product_name %}-Benutzernamen oder Deine E-Mail-Adresse ein.
    - Gib im zweiten Feld den Text von der Aufforderung ein.
