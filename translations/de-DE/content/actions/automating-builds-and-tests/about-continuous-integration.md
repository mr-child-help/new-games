---
title: Informationen zur fortlaufenden Integration
intro: 'You can create custom continuous integration (CI) workflows directly in your {% data variables.product.prodname_dotcom %} repository with {% data variables.product.prodname_actions %}.'
redirect_from:
  - /articles/about-continuous-integration
  - /github/automating-your-workflow-with-github-actions/about-continuous-integration
  - /actions/automating-your-workflow-with-github-actions/about-continuous-integration
  - /actions/building-and-testing-code-with-continuous-integration/about-continuous-integration
  - /actions/guides/about-continuous-integration
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: overview
topics:
  - CI
shortTitle: Kontinuierliche Integration
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

## Informationen zur fortlaufenden Integration

Bei der Softwarepraktik der fortlaufenden Integration (CI) erfolgen häufige Code-Commits an ein gemeinsames Repository. Code-Commits in kurzen Abständen tragen dazu bei, Fehler frühzeitiger aufzudecken, und verringern die Codemenge, die ein Entwickler auf der Suche nach der Fehlerursache debuggen muss. Durch häufige Code-Aktualisierungen lassen sich zudem Änderungen von verschiedenen Mitgliedern eines Software-Entwicklungsteams leichter zusammenführen. Dies bedeutet einen erheblichen Vorteil für die Entwickler, die sich damit stärker auf das Schreiben des Codes konzentrieren können, statt Fehler debuggen oder Mergekonflikte beheben zu müssen.

Durch einen Code-Commit an das Repository können Sie den Code fortlaufend erstellen und testen, sodass gewährleistet ist, dass der Commit keine Fehler einbringt. Die Tests können beispielsweise Code-Linters (überprüfen Stilformatierungen), Sicherheitsprüfungen, Code-Abdeckung, Funktionstests und andere benutzerdefinierte Prüfungen umfassen.

Zum Erstellen und Testen des Codes ist ein Server erforderlich. Sie können Aktualisierungen lokal erstellen und testen, bevor Sie den Code per Push an ein Repository senden, oder auch einen CI-Server heranziehen, der neue Code-Commits in einem Repository prüft.

## Informationen zur kontinuierlichen Integration mit {% data variables.product.prodname_actions %}

{% ifversion ghae %}CI using {% data variables.product.prodname_actions %} offers workflows that can build the code in your repository and run your tests. Workflows can run on virtual machines hosted by {% data variables.product.prodname_dotcom %}. For more information, see "[About {% data variables.actions.hosted_runner %}s](/actions/using-github-hosted-runners/about-ae-hosted-runners)."
{% else %} CI using {% data variables.product.prodname_actions %} offers workflows that can build the code in your repository and run your tests. Workflows können auf {% data variables.product.prodname_dotcom %}gehosteten virtuellen Maschinen oder auf Computern ausgeführt werden, die Sie selbst hosten. For more information, see "[Virtual environments for {% data variables.product.prodname_dotcom %}-hosted runners](/actions/automating-your-workflow-with-github-actions/virtual-environments-for-github-hosted-runners)" and "[About self-hosted runners](/actions/automating-your-workflow-with-github-actions/about-self-hosted-runners)."
{% endif %}

Sie können den CI-Workflow so konfigurieren, dass er bei einem {% data variables.product.prodname_dotcom %}-Ereignis (z. B. wenn neuer Code per Push in das Repository eingebracht wird), nach einem festen Zeitplan oder bei einem externen Ereignis anhand des Sende-Webhooks des Repositorys ausgeführt wird.

{% data variables.product.product_name %} führt die CI-Tests aus und stellt die Ergebnisse jedes Tests in der Pullanforderung bereit, sodass Sie sehen können, ob die Änderung in Ihrem Zweig einen Fehler verursacht. Sobald alle CI-Tests in einem Workflow bestanden wurden, können die per Push übermittelten Änderungen von einem Teammitglied geprüft oder zusammengeführt werden. Wenn ein Test nicht bestanden wird, liegt die Ursache eventuell in einer Ihrer Änderungen.

Wenn Sie CI in Ihrem Repository einrichten, analysiert {% data variables.product.product_name %} den Code in Ihrem Repository und empfiehlt CI-Workflows basierend auf der Sprache und dem Framework in Ihrem Repository. Wenn Sie beispielsweise [Node.js](https://nodejs.org/en/)verwenden, schlägt {% data variables.product.product_name %} eine Vorlagendatei vor, die Ihre Node.js-Pakete installiert und Ihre Tests ausführt. Sie können die von {% data variables.product.product_name %}vorgeschlagene CI-Workflowvorlage verwenden, die vorgeschlagene Vorlage anpassen oder eine eigene benutzerdefinierte Workflowdatei zum Ausführen der CI-Tests erstellen.

![Screenshot mit vorgeschlagenen Vorlagen für die fortlaufende Integration](/assets/images/help/repository/ci-with-actions-template-picker.png)

Sie können nicht nur ci-Workflows für Ihr Projekt einrichten, sondern auch {% data variables.product.prodname_actions %} verwenden, um Workflows über den gesamten Softwareentwicklungslebenszyklus hinweg zu erstellen. Sie können Ihr Projekt beispielsweise mithilfe von Aktionen bereitstellen, packen oder veröffentlichen. Weitere Informationen finden Sie unter "[über {% data variables.product.prodname_actions %}](/articles/about-github-actions)".

Eine Definition von gebräuchliche Begriffe finden Sie unter "[Kernkonzepte für {% data variables.product.prodname_actions %}](/github/automating-your-workflow-with-github-actions/core-concepts-for-github-actions)".

## Workflow templates

{% data variables.product.product_name %} bietet CI-Workflowvorlagen für eine Vielzahl von Sprachen und Frameworks.

Browse the complete list of CI workflow templates offered by {% data variables.product.company_short %} in the {% ifversion fpt or ghec %}[actions/starter-workflows](https://github.com/actions/starter-workflows/tree/main/ci) repository{% else %} `actions/starter-workflows` repository on {% data variables.product.product_location %}{% endif %}.

## Weiterführende Informationen

{% ifversion fpt or ghec %}
- "[ Abrechnung für {% data variables.product.prodname_actions %} verwalten](/billing/managing-billing-for-github-actions)"
{% endif %}
