---
title: Unterhaltungen sperren
intro: 'Repository-Inhaber und -Mitarbeiter sowie Personen mit Schreibzugriff auf ein Repository können Unterhaltungen zu Issues, Pull-Requests und Commits dauerhaft oder temporär sperren, um eine hitzige Diskussion zu entschärfen.'
redirect_from:
  - /articles/locking-conversations
  - /github/building-a-strong-community/locking-conversations
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Community
---

Es ist angemessen, eine Unterhaltung zu sperren, wenn die gesamte Unterhaltung nicht konstruktiv ist oder den Verhaltenskodex Deiner Community{% ifversion fpt or ghec %} oder die [Community-Richtlinien](/free-pro-team@latest/github/site-policy/github-community-guidelines) von GitHub{% endif %} verletzen. Wenn Du eine Unterhaltung sperrst, kannst Du auch einen Grund dafür angeben, der dann öffentlich sichtbar ist.

Das Sperren einer Unterhaltung erstellt ein Zeitleistenereignis, das für alle Benutzer mit Lesezugriff auf das Repository sichtbar ist. Der Benutzername der Person, die die Unterhaltung gesperrt hat, ist jedoch nur für Benutzer mit Schreibzugriff auf das Repository zu sehen. Für Personen ohne Schreibzugriff ist das Zeitleistenereignis anonymisiert.

![Anonymisiertes Zeitleistenereignis für eine gesperrte Unterhaltung](/assets/images/help/issues/anonymized-timeline-entry-for-locked-conversation.png)

Solange eine Unterhaltung gesperrt ist, können nur [Personen mit Schreibzugriff](/articles/repository-permission-levels-for-an-organization/) und [Repository-Inhaber und -Mitarbeiter](/articles/permission-levels-for-a-user-account-repository/#collaborator-access-for-a-repository-owned-by-a-user-account) Kommentare hinzufügen, ausblenden und löschen.

Um nach gesperrten Unterhaltungen in einem nicht archivierten Repository zu suchen, kannst Du die Qualifizierer `is:locked` und `archived:false` verwenden. In archivierten Repositorys sind Unterhaltungen automatisch gesperrt. Weitere Informationen findest Du unter „[Issues und Pull Requests durchsuchen](/search-github/searching-on-github/searching-issues-and-pull-requests#search-based-on-whether-a-conversation-is-locked).“

1. Verfasse optional einen Kommentar, in dem Du erklärst, weshalb Du die Unterhaltung sperrst.
2. Klicke am rechten Rand des Issues respektive Pull Requests oder oberhalb des Kommentarfelds auf der Commit-Seite auf **Lock conversation** (Unterhaltung sperren). ![Link „Lock conversation“ (Unterhaltung sperren)](/assets/images/help/repository/lock-conversation.png)
3. Optional kannst Du einen Grund für das Sperren der Unterhaltung auswählen. ![Menü „Reason for locking a conversation" (Grund für das Sperren einer Unterhaltung)](/assets/images/help/repository/locking-conversation-reason-menu.png)
4. Lies die Informationen zum Sperren von Unterhaltungen, und klicke auf **Lock conversation on this issue** (Unterhaltung zu diesem Issue sperren), **Lock conversation on this pull request** (Unterhaltung zu diesem Pull Request sperren) oder **Lock conversation on this commit** (Unterhaltung zu diesem Commit sperren). ![Dialogfeld „Confirm lock with a reason" (Bestätigen der Sperre mit Begründung)](/assets/images/help/repository/lock-conversation-confirm-with-reason.png)
5. Wenn Du die Sperre der Unterhaltung beenden möchtest, klicke auf **Unlock conversation** (Unterhaltung entsperren). ![Link „Unlock conversation“ (Unterhaltung entsperren)](/assets/images/help/repository/unlock-conversation.png)

## Weiterführende Informationen

- „[Dein Projekt für sinnvolle Beiträge einrichten](/communities/setting-up-your-project-for-healthy-contributions)“
- „[Vorlagen benutzen, um hilfreiche Issues und Pull Requests zu ermutigen](/communities/using-templates-to-encourage-useful-issues-and-pull-requests)"
- „[Störende Kommentare verwalten](/communities/moderating-comments-and-conversations/managing-disruptive-comments)"{% ifversion fpt or ghec %}
- „[Deine Sicherheit auf {% data variables.product.prodname_dotcom %} aufrechterhalten](/communities/maintaining-your-safety-on-github)"
- „[Missbrauch oder Spam melden](/communities/maintaining-your-safety-on-github/reporting-abuse-or-spam)“
- „[Interaktionen in Deinem Repository einschränken](/communities/moderating-comments-and-conversations/limiting-interactions-in-your-repository)"
{% endif %}
