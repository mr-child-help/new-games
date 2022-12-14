---
title: Informationen zum Vergleich von Branches in Pull Requests
intro: 'In Pull Requests werden Diffs angezeigt, um die Änderungen, die Du in Deinem Themen-Branch vorgenommen hast, mit dem Basis-Branch zu vergleichen, in den du Deine Änderungen zusammenführen möchtest.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-comparing-branches-in-pull-requests
  - /articles/about-comparing-branches-in-pull-requests
  - /github/collaborating-with-issues-and-pull-requests/about-comparing-branches-in-pull-requests
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Compare branches
---

{% note %}

**Hinweis:** Beim Erstellen Deines Pull Requests kannst Du den Basis-Branch ändern, gegen den Du Deine Änderungen vergleichst. Weitere Informationen findest Du unter „[Einen Pull Request erstellen](/articles/creating-a-pull-request#changing-the-branch-range-and-destination-repository).“

{% endnote %}

You can view proposed changes in a pull request in the Files changed tab. ![Registerkarte für geänderte Pull-Request-Dateien](/assets/images/help/pull_requests/pull-request-tabs-changed-files.png)

Anstatt die Commits selbst anzuzeigen, können Sie die vorgeschlagenen Änderungen so anzeigen, wie sie in den Dateien erscheinen, sobald der Pull Request gemergt wurde. Die Dateien werden in alphabetischer Reihenfolge auf der Registerkarte „Files changed“ (Geänderte Dateien) angezeigt. Ergänzungen zu den Dateien erscheinen grün und sind durch ein „`+`“-Zeichen gekennzeichnet , wohingegen entfernte Inhalte rot erscheinen und durch ein „`-`“-Zeichen gekennzeichnet sind.

## Anzeigeoptionen für Diffs

{% tip %}

**Tipp:** Wenn Sie den Kontext einer Änderung nicht nachvollziehen können, können Sie auf der Registerkarte „Files changed“ (Geänderte Dateien) auf **View** (Anzeigen) klicken, um die gesamte Datei mit den vorgeschlagenen Änderungen anzuzeigen.

{% endtip %}

Sie haben mehrere Möglichkeiten für die Anzeige eines Diff:
- Die einheitliche Ansicht zeigt aktualisierte und vorhandene Inhalte gemeinsam in einer linearen Ansicht.
- Die geteilte Ansicht zeigt alte Inhalte auf der einen Seite und neue Inhalte auf der anderen Seite.
- Die Rich-Diff-Ansicht zeigt eine Vorschau, wie die Änderungen nach dem Merge des Pull Requests aussehen werden.
- Die Quellansicht zeigt die Änderungen in der Quelle ohne die Formatierung der Rich-Diff-Ansicht.

Sie können außerdem Leerzeichenänderungen ignorieren, um eine genauere Ansicht der wesentlichen Änderungen in einem Pull Request zu erhalten.

![Menü mit Diff-Anzeigeoptionen](/assets/images/help/pull_requests/diff-settings-menu.png)

To simplify reviewing changes in a large pull request, you can filter the diff to only show selected file types, show files you are a CODEOWNER of, hide files you have already viewed, or hide deleted files. Weitere Informationen findest Du unter „[Dateien in einem Pull Request nach Dateityp filtern](/articles/filtering-files-in-a-pull-request).“

  ![Dropdownmenü mit Dateifiltern](/assets/images/help/pull_requests/file-filter-menu.png)

## Vergleiche von Three-Dot- (Dreipunkte-) und Two-Dot- (Zweipunkte-) Diffs von Git

Standardmäßig zeigen Pull-Requests auf {% data variables.product.prodname_dotcom %} einen three-dot-Diff (Dreipunkte-Diff) an, oder einen Vergleich zwischen der aktuellsten Version des Themenzweiges und dem Commit, in dem der Themenzweig letztmals mit dem Basis-Zweig synchronisiert wurde.

Um zwei Committish-Referenzen in einem Two-Dot-Diff-Vergleich auf {% data variables.product.prodname_dotcom %} zu sehen, kannst Du die URL der Seite „Comparing changes“ (Änderungen vergleichen) Deines Repositorys bearbeiten. Weitere Informationen findest Du im  [Git-Glossareintrag zu „Committish“](https://git-scm.com/docs/gitglossary#gitglossary-aiddefcommit-ishacommit-ishalsocommittish) auf der Buchseite _Pro Git_.

{% data reusables.repositories.two-dot-diff-comparison-example-urls %}

Ein Two-Dot-Diff vergleicht zwei Git-Committish-Referenzen, wie SHAs oder OIDs (Objekt-IDs), direkt miteinander. Auf {% data variables.product.prodname_dotcom %} müssen die Git-Committish-Referenzen in einem Two-Dot-Diff-Vergleich an das gleiche Repository oder seine Forks gepusht werden.

Wenn Sie einen Two-Dot-Diff in einem Pull Request simulieren und einen Vergleich zwischen den neuesten Versionen jedes Branch sehen möchten, können Sie den Basis-Branch in Ihren Themen-Branch mergen, wodurch der letzte gemeinsame Vorgänger Ihrer Branches aktualisiert wird.

For more information about Git commands to compare changes, see "[Git diff options](https://git-scm.com/docs/git-diff#git-diff-emgitdiffemltoptionsgtltcommitgtltcommitgt--ltpathgt82308203)" from the _Pro Git_ book site.

## Gründe für Anzeigefehler bei Diffs
- Du hast die maximale Anzahl von Dateien oder bestimmten Dateitypen überschritten. For more information, see "[About repositories](/repositories/creating-and-managing-repositories/about-repositories#limits-for-viewing-content-and-diffs-in-a-repository)."
- Deine Datei entspricht einer Regel in der *.gitattributes*-Datei des Repositorys, welche verhindert, dass diese Datei standardmäßig angezeigt wird. Weitere Informationen findest Du unter „[Darstellung geänderter Dateien auf GitHub anpassen](/articles/customizing-how-changed-files-appear-on-github).“

## Weiterführende Informationen

- „[Informationen zu Pull Requests](/articles/about-pull-requests)“
- „[Informationen zu Forks](/articles/about-forks)“
