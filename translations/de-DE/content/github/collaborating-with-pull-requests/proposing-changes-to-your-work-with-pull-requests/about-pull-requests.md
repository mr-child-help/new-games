---
title: Informationen zu Pull Requests
intro: 'Mit Pull Requests können Sie andere Benutzer über Änderungen informieren, die Sie an einen Branch in einem Repository auf {% data variables.product.product_name %} gepusht haben. Sobald ein Pull Request geöffnet ist, kannst Du die potenziellen Änderungen mit Mitarbeitern diskutieren und überprüfen und Follow-up-Commits hinzufügen, bevor Deine Änderungen in den Basis-Branch übertragen werden.'
redirect_from:
  - /github/collaborating-with-issues-and-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests
  - /articles/using-pull-requests/
  - /articles/about-pull-requests
  - /github/collaborating-with-issues-and-pull-requests/about-pull-requests
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pull requests
---

## Informationen zu Pull Requests

{% note %}

**Hinweis:** Beachte bei der Arbeit mit Pull Requests Folgendes:
* Wenn Du mit dem [Modell für gemeinsame Repositorys](/articles/about-collaborative-development-models) arbeitest, empfehlen wir Dir, für Deinen Pull Request einen Themen-Branch zu verwenden. Zwar kannst Du Pull Requests von jedem Branch oder Commit aus senden, aber mit einem Themen-Branch kannst Du Follow-up-Commits übertragen, wenn Du Deine vorgeschlagenen Änderungen aktualisieren musst.
* Erzwinge keinen Push beim Übertragen von Commits an einen Pull Request. Ein erzwungener Push kann Deinen Pull Request beschädigen.

{% endnote %}

You can create pull requests on {% data variables.product.prodname_dotcom_the_website %}, with {% data variables.product.prodname_desktop %}, in {% data variables.product.prodname_codespaces %}, on {% data variables.product.prodname_mobile %}, and when using GitHub CLI.

Nach der Initialisierung eines Pull Requests siehst Du eine Review-Seite, die einen detaillierten Überblick über die Änderungen zwischen Deinem Branch (dem Vergleichs-Branch) und dem Basis-Branch des Repositorys bietet. Du kannst eine Zusammenfassung der vorgeschlagenen Änderungen hinzufügen, die durch Commits vorgenommenen Änderungen überprüfen, Kennzeichnungen, Meilensteine und Bearbeiter hinzufügen und einzelne Mitarbeiter oder Teams @erwähnen. Weitere Informationen findest Du unter „[Einen Pull Request erstellen](/articles/creating-a-pull-request).“

Sobald Du einen Pull Request erstellt hast, kannst Du Commits aus Deinem Themen-Branch übertragen, um sie zu Deinem bestehenden Pull Request hinzuzufügen. Diese Commits werden in chronologischer Reihenfolge in Deinem Pull Request angezeigt, und die Änderungen sind auf der Registerkarte „Files changed“ (Dateien geändert) sichtbar.

Andere Mitarbeiter können Deine vorgeschlagenen Änderungen überprüfen, Review-Kommentare hinzufügen, zur Diskussion über den Pull Request beitragen und sogar Commits zum Pull Request hinzufügen.

{% ifversion fpt or ghec %}
Auf der Registerkarte „Conversation“ (Unterhaltung) siehst Du Informationen über den aktuellen Bereitstellungsstatus des Branches und vergangene Bereitstellungsaktivitäten. Weitere Informationen findest Du unter „[Bereitstellungsaktivitäten für ein Repository anzeigen](/repositories/viewing-activity-and-data-for-your-repository/viewing-deployment-activity-for-your-repository).“
{% endif %}

Wenn Du mit den vorgeschlagenen Änderungen einverstanden bist, kannst Du den Pull Request zusammenführen. Wenn Du in einem Modell mit gemeinsamen Repositorys arbeitest, erstellst Du einen Pull Request und Du oder jemand anders wird Deine Änderungen von Deinem Funktions-Branch in den Basis-Branch zusammenführen, den Du im Pull Request angegeben hast. Weitere Informationen findest Du unter „[Einen Pull Request zusammenführen](/articles/merging-a-pull-request).“

{% data reusables.pull_requests.required-checks-must-pass-to-merge %}

{% data reusables.pull_requests.close-issues-using-keywords %}

{% tip %}

**Tipps:**
- Um zwischen der reduzierten oder erweiterten Anzeige aller veralteten Review-Kommentare in einem Pull Request umzuschalten, drücke <span class="platform-mac"><kbd>option</kbd></span><span class="platform-linux"><kbd>Alt</kbd></span><span class="platform-windows"><kbd>Alt</kbd></span> und klicke auf **Show outdated** (Zeige veraltete an) oder **Hide outdated** (Blende veraltete aus). Weitere Kürzel findest Du unter „[Tastenkürzel](/articles/keyboard-shortcuts).“
- Du kannst beim Zusammenführen eines Pull Requests Commits squashen, um eine optimierte Ansicht der Änderungen zu erhalten. Weitere Informationen findest Du unter „[Informationen zum Zusammenführen von Pull Requests](/articles/about-pull-request-merges).“

{% endtip %}

In Deinem Dashboard findest Du schnell Links zu zuletzt aktualisierten Pull Requests, an denen Du gerade arbeitest oder die Du abonniert hast. Weitere Informationen findest Du unter „[Informationen zum persönlichen Dashboard](/articles/about-your-personal-dashboard).“

## Entwürfe für Pull Requests

{% data reusables.gated-features.draft-prs %}

Wenn Du einen Pull Request erstellst, kannst Du wählen, ob Du einen für den Review bereiten Pull Request oder einen Pull-Request-Entwurf erstellen möchten. Pull-Request-Entwürfe können nicht zusammengeführt werden, und Code-Inhaber werden nicht automatisch aufgefordert, Pull-Request-Entwürfe zu überprüfen. Weitere Informationen zum Erstellen eines Pull-Request-Entwurfs findest Du unter „[Einen Pull Request erstellen](/articles/creating-a-pull-request)“ und „[Einen Pull Request von einem Fork erstellen](/articles/creating-a-pull-request-from-a-fork).“

{% data reusables.pull_requests.mark-ready-review %} Du kannst einen Pull Request jederzeit in einen Entwurf umwandeln. Weitere Informationen findest Du unter „[Den Zustand eines Pull Requests ändern](/articles/changing-the-stage-of-a-pull-request).“

## Differences between commits on compare and pull request pages

The compare and pull request pages use different methods to calculate the diff for changed files:

- Compare pages show the diff between the tip of the head ref and the current common ancestor (that is, the merge base) of the head and base ref.
- Pull request pages show the diff between the tip of the head ref and the common ancestor of the head and base ref at the time when the pull request was created. Consequently, the merge base used for the comparison might be different.

## Weiterführende Informationen

- „[Pull Request](/articles/github-glossary/#pull-request)“ im {% data variables.product.prodname_dotcom %}-Glossar
- „[Informationen zu Branches](/articles/about-branches)“
- „[Einen Pull Request kommentieren](/articles/commenting-on-a-pull-request)“
- „[Einen Pull Request schließen](/articles/closing-a-pull-request)“
