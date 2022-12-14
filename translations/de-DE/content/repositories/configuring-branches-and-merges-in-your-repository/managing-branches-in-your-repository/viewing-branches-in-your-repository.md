---
title: Branches in Deinem Repository anzeigen
intro: 'Branches sind entscheidend für die Zusammenarbeit auf {% data variables.product.product_name %}. Sie lassen sich bestmöglich auf der Branches-Seite anzeigen.'
redirect_from:
  - /articles/viewing-branches-in-your-repository
  - /github/administering-a-repository/viewing-branches-in-your-repository
  - /github/administering-a-repository/managing-branches-in-your-repository/viewing-branches-in-your-repository
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Repositories
shortTitle: View branches
---

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.navigate-to-branches %}
3. Mithilfe der im oberen Bereich der Seite befindlichen Navigation kannst Du spezifische Listen der Branches anzeigen:
    - **Your branches**: In repositories that you have push access to, the **Yours** view shows all branches that you’ve pushed to, excluding the default branch, with the most recent branches first.
    - **Active branches** (Aktive Branches): Die Ansicht **Active** (Aktiv) zeigt alle Branches an, zu denen in den letzten drei Monaten Commits beigetragen wurden, wobei die Branches mit den neuesten Commits zuerst angezeigt werden.
    - **Stale branches** (Alte Branches): Die Ansicht **Stale** (Alt) zeigt alle Branches an, zu denen in den letzten drei Monaten keine Commits beigetragen wurden, wobei die Branches mit den ältesten Commits zuerst angezeigt werden. Verwende diese Liste, um zu bestimmen, [welche Branches gelöscht werden sollen](/articles/creating-and-deleting-branches-within-your-repository).
    - **All branches** (Alle Branches): Die Ansicht **All** (Alle) zeigt den Standardbranch, gefolgt von allen anderen Branches, wobei die Branches mit den neuesten Commits zuerst angezeigt werden.

4. Optionally, use the search field on the top right. It provides a simple, case-insensitive, sub-string search on the branch name. It does not support any additional query syntax.

![Die Branches-Seite für das Atom-Repository](/assets/images/help/branches/branches-overview-atom.png)

## Weiterführende Informationen

- „[Branches in Ihrem Repository erstellen und löschen](/articles/creating-and-deleting-branches-within-your-repository)“
- „[Nicht verwendete Branches löschen](/articles/deleting-unused-branches)“
