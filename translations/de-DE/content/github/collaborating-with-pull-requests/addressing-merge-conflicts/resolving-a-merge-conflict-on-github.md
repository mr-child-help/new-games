---
title: Mergekonflikt auf GitHub beheben
intro: 'Einfache Mergekonflikte auf GitHub, bei denen Zeilenänderungen in Konflikt stehen, kannst Du mit dem Konflikteditor beheben.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/addressing-merge-conflicts/resolving-a-merge-conflict-on-github
  - /articles/resolving-a-merge-conflict-on-github
  - /github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-on-github
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
shortTitle: Resolve merge conflicts
---

Auf {% data variables.product.product_name %} können Sie nur Mergekonflikte beheben, die durch konkurrierende Zeilenänderungen verursacht werden, beispielsweise, wenn mehrere Personen unterschiedliche Änderungen an der gleichen Zeile in der gleichen Datei in verschiedenen Branches Ihres Git-Repositorys vornehmen. Alle anderen Mergekonflikte musst Du lokal in der Befehlszeile beheben. Weitere Informationen findest Du unter „[Einen Mergekonflikt in der Befehlszeile beheben](/articles/resolving-a-merge-conflict-using-the-command-line/).“

{% ifversion ghes or ghae %}
Wenn ein Websiteadministrator den Editor für Mergekonflikte für Pull Requests zwischen Repositorys deaktiviert, können Sie den Konflikteditor auf {% data variables.product.product_name %} nicht verwenden. Mergekonflikte müssen Sie dann in der Befehlszeile beheben. Beispielsweise können Sie den Mergekonflikteditor, sofern er deaktiviert ist, nicht für Pull Requests zwischen einem Fork und einem vorgelagerten Repository verwenden.
{% endif %}

{% warning %}

**Warnung:** Wenn Du einen Mergekonflikt auf {% data variables.product.product_name %} auflöst, wird der gesamte [Basis-Branch](/github/getting-started-with-github/github-glossary#base-branch) Deines Pull Requests in den [Head-Branch](/github/getting-started-with-github/github-glossary#head-branch) zusammengeführt. Vergewissern Sie sich, dass es wirklich dieser Branch ist, den Sie festschreiben möchten. If the head branch is the default branch of your repository, you'll be given the option of creating a new branch to serve as the head branch for your pull request. Wenn der Head-Branch geschützt ist, kannst Du Deine Konflikt-Auflösung nicht zusammenführen, deshalb wirst Du aufgefordert werden, einen neuen Head-Branch zu erstellen. Weitere Informationen findest Du unter „[Informationen zu geschützten Branches](/github/administering-a-repository/about-protected-branches).“

{% endwarning %}

{% data reusables.repositories.sidebar-pr %}
1. Klicke in der Liste der Pull Requests auf den Pull Request mit dem Mergekonflikt, den Du beheben möchtest.
1. Klicke im unteren Teil Deines Pull Requests auf **Resolve conflicts** (Konflikte beheben). ![Schaltfläche „Resolve merge conflicts" (Mergekonflikte beheben)](/assets/images/help/pull_requests/resolve-merge-conflicts-button.png)

 {% tip %}

 **Tipp:** Wenn die Schaltfläche **Resolve conflicts** (Konflikte beheben) deaktiviert ist, ist der Mergekonflikt Deines Pull Requests für eine Behebung auf {% data variables.product.product_name %} zu komplex{% ifversion ghes or ghae %} oder der Konflikteditor wurde vom Websiteadministrator für Pull Requests zwischen Repositorys deaktiviert{% endif %}. Du musst den Mergekonflikt mit einem alternativen Git-Client auflösen, oder durch Verwendung von Git auf der Befehlszeile. Weitere Informationen findest Du unter „[Mergekonflikt in der Befehlszeile beheben](/articles/resolving-a-merge-conflict-using-the-command-line).“

 {% endtip %}
{% data reusables.pull_requests.decide-how-to-resolve-competing-line-change-merge-conflict %}
 ![Beispiel für die Anzeige eines Mergekonflikts mit Konflikthinweisen](/assets/images/help/pull_requests/view-merge-conflict-with-markers.png)
1. Wenn Deine Datei mehrere Mergekonflikte enthält, scrolle nach unten zum nächsten Konflikthinweis, und wiederhole dort die Schritte 4 und 5, um auch diesen Mergekonflikt zu beheben.
1. Wenn Du alle Konflikte in der Datei behoben hast, klicke auf **Mark as resolved** (Als behoben markieren). ![Klicke die Schaltfläche „Mark as resolved“ (Als behoben markieren)](/assets/images/help/pull_requests/mark-as-resolved-button.png)
1. Wenn mehrere Dateien Konflikte enthalten, wähle auf der linken Seite unter „Conflicting files“ (Dateien mit Konflikten) die nächste Datei aus, und wiederhole die Schritte 4 bis 7, bis Du alle Mergekonflikte Deines Pull Request behoben hast. ![Wähle die nächste Datei mit Konflikten aus, sofern zutreffend](/assets/images/help/pull_requests/resolve-merge-conflict-select-conflicting-file.png)
1. Wenn alle Mergekonflikte behoben sind, klicke auf **Commit merge** (Merge freigeben). Dadurch wird der gesamte Basis-Branch in Deinen Head-Branch zusammengeführt. ![Schaltfläche „Resolve merge conflicts" (Mergekonflikte beheben)](/assets/images/help/pull_requests/merge-conflict-commit-changes.png)
1. Sofern Du eine entsprechende Aufforderung erhältst, überprüfe den Branch, in den der Commit erfolgt.

   Wenn der Head-Branch der Standardbranch Deines Repositorys ist, kannst Du wählen, entweder diesen Branch mit den Änderungen zu aktualisieren, die Du zur Auflösung des Konfliktes gemacht hast, oder einen neuen Branch zu erstellen und diesen als Head-Branch des Pull Requests zu verwenden. ![Aufforderung zum Überprüfen des Branch, der aktualisiert wird](/assets/images/help/pull_requests/conflict-resolution-merge-dialog-box.png)

   Wenn Du Dich für einen neuen Branch entscheidest, gib den Namen für den Branch ein.

   Wenn der Head-Branch Deines Pull-Requests geschützt ist, musst Du einen neuen Branch erstellen. Du hast keine Möglichkeit, den geschützten Branch zu aktualisieren.

   Klicke auf **Create branch and update my pull request** (Erstelle den Branch und aktualisiere meinen Pull Request) oder **I understand, continue updating _BRANCH_** (Ich verstehe, bitte mit der Aktualisierung des BRANCH fortfahren). Der Text der Schaltfläche entspricht der Aktion, die Du durchführst.
1. Zum Zusammenführen Deines Pull Requests klicke auf **Merge pull request** (Pull Request zusammenführen). Weitere Informationen finden Sie unter „[Pull Request mergen](/articles/merging-a-pull-request/)“.

## Weiterführende Informationen

- „[Informationen zum Mergen von Pull Requests](/articles/about-pull-request-merges)“
