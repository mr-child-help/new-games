---
title: About custom actions
intro: 'Aktionen sind einzelne Aufgaben, die Du kombinieren kannst, um Aufträge zu erstellen und Deinen Workflow anzupassen. You can create your own actions, or use and customize actions shared by the {% data variables.product.prodname_dotcom %} community.'
redirect_from:
  - /articles/about-actions
  - /github/automating-your-workflow-with-github-actions/about-actions
  - /actions/automating-your-workflow-with-github-actions/about-actions
  - /actions/building-actions/about-actions
  - /actions/creating-actions/about-actions
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: overview
topics:
  - Action development
  - Fundamentals
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

## About custom actions

Zum Erstellen von Aktionen Kannst Du benutzerdefinierten Code schreiben, der mit Deinem Repository auf die gewünschte Weise interagiert und sich dabei beispielsweise in die APIs von {% data variables.product.prodname_dotcom %} und in öffentlich zugängliche Drittanbieter-APIs integriert. Mit einer Aktion können Sie beispielsweise npm-Module veröffentlichen, SMS-Nachrichten bei dringenden Problemen senden oder produktionsreifen Code bereitstellen.

{% ifversion fpt or ghec %}
Sie können eigene Aktionen schreiben und ausschließlich in Ihrem Workflow verwenden oder auch Ihre erstellten Aktionen mit der {% data variables.product.prodname_dotcom %}-Community schreiben. Die erstellten Aktionen können nur dann freigegeben werden, wenn das Repository öffentlich ist.
{% endif %}

Aktionen können direkt auf einem Computer oder in einem Docker-Container laufen. Sie können die Eingabe, die Ausgabe und die Umgebungsvariablen für eine Aktion definieren.

## Arten von Aktionen

Sie können Docker-Container- und JavaScript-Aktionen erstellen. Für Aktionen wird eine Metadaten-Datei benötigt, in der die Eingaben, Ausgaben und der Haupteinstiegspunkt für die Aktion definiert werden. Der Dateiname für die Metadaten muss entweder `action.yml` oder `action.yaml` sein. Weitere Informationen findest Du unter „[Metadatensyntax für {% data variables.product.prodname_actions %}](/articles/metadata-syntax-for-github-actions)“.

| Typ               | Betriebssystem        |
| ----------------- | --------------------- |
| Docker-Container  | Linux                 |
| JavaScript        | Linux, macOS, Windows |
| Composite Actions | Linux, macOS, Windows |

### Docker-Containeraktionen

Docker-Container paketieren die Umgebung mit dem {% data variables.product.prodname_actions %}-Code. So entsteht eine konsistentere, zuverlässigere Arbeitseinheit, da der Aktionsbenutzer sich nicht um Tools oder Abhängigkeiten kümmern muss.

Mit einem Docker-Container können Sie bestimmte Versionen eines Betriebssystems sowie bestimmte Abhängigkeiten, Tools und Code verwenden. Bei Aktionen, die in einer bestimmten Umgebungskonfiguration ausgeführt werden müssen, ist Docker eine ideale Option, da Sie das Betriebssystem und die Tools anpassen können. Wegen der Latenz für das Erstellen und Abrufen des Containers sind Docker-Container-Aktionen langsamer als JavaScript-Aktionen.

Docker Container-Aktionen können nur auf Runnern mit einem Linux-Betriebssystem ausgeführt werden. {% data reusables.github-actions.self-hosted-runner-reqs-docker %}

### JavaScript-Aktionen

JavaScript-Aktionen können direkt auf einem Runner-Rechner laufen und den Aktions-Code von der Umgebung trennen, in der der Code läuft. Eine JavaScript-Aktion umfasst einfacheren Aktionscode und lässt sich schneller ausführen als eine Docker-Container-Aktion.

{% data reusables.github-actions.pure-javascript %}

Wenn Sie ein Node.js Projekt entwickeln, bietet das {% data variables.product.prodname_actions %} Toolkit Pakete, die Sie in Ihrem Projekt verwenden können, um die Entwicklung zu beschleunigen. Weitere Informationen findest Du im Repository [actions/toolkit](https://github.com/actions/toolkit).

### Composite Actions

A _composite_ action allows you to combine multiple workflow steps within one action. For example, you can use this feature to bundle together multiple run commands into an action, and then have a workflow that executes the bundled commands as a single step using that action. To see an example, check out "[Creating a composite action](/actions/creating-actions/creating-a-composite-action)".

## Ort für eine Aktion auswählen

Wenn Du eine Aktion entwickelst, die von anderen Personen genutzt werden soll, empfehlen wir, die Aktion in ihrem eigenen Repository zu belassen, also nicht mit anderem Anwendungscode zu einem Bundle zusammenzufassen. Damit kannst Du die Aktion wie jede andere Software versionieren, nachverfolgen und veröffentlichen.

{% ifversion fpt or ghec %}
Wenn Sie eine Aktion in einem eigenen Repository speichern, kann die {% data variables.product.prodname_dotcom %}-Community die Aktion eher entdecken. Außerdem wird damit die Codebasis begrenzt, auf die die Entwickler bei der Fehlerbehebung und bei der Erweiterung der Aktion angewiesen sind, und die Versionierung der Aktion wird von der Versionierung des anderen Anwendungscodes getrennt.
{% endif %}

{% ifversion fpt or ghec %}If you're building an action that you don't plan to make available to the public, you {% else %} You{% endif %} can store the action's files in any location in your repository. Wenn der Aktions-, der Workflow- und der Anwendungscode in einem einzigen Repository abgelegt werden sollen, empfehlen wir, die Aktionen im Verzeichnis `.github` zu speichern. Beispiel: `.github/actions/action-a` und `.github/actions/action-b`.

## Compatibility with {% data variables.product.prodname_ghe_server %}

To ensure that your action is compatible with {% data variables.product.prodname_ghe_server %}, you should make sure that you do not use any hard-coded references to {% ifversion fpt or ghec %}{% data variables.product.prodname_dotcom %}{% else %}{% data variables.product.product_name %}{% endif %} API URLs. You should instead use environment variables to refer to the {% ifversion fpt or ghec %}{% data variables.product.prodname_dotcom %}{% else %}{% data variables.product.product_name %}{% endif %} API:

- Verwenden Sie für die REST-API die `GITHUB_API_URL` -Umgebungsvariable.
- Verwenden Sie für GraphQL die Umgebungsvariable `GITHUB_GRAPHQL_URL` .

For more information, see "[Default environment variables](/actions/configuring-and-managing-workflows/using-environment-variables#default-environment-variables)."

## Using release management for actions

This section explains how you can use release management to distribute updates to your actions in a predictable way.

### Good practices for release management

If you're developing an action for other people to use, we recommend using release management to control how you distribute updates. Users can expect an action's major version to include necessary critical fixes and security patches, while still remaining compatible with their existing workflows. You should consider releasing a new major version whenever your changes affect compatibility.

Bei diesem Releaseverwaltungsansatz sollten Benutzer nicht auf den `Master` Zweig einer Aktion verweisen, da dieser wahrscheinlich den neuesten Code enthält und daher möglicherweise instabil ist. Instead, you can recommend that your users specify a major version when using your action, and only direct them to a more specific version if they encounter issues.

To use a specific action version, users can configure their {% data variables.product.prodname_actions %} workflow to target a tag, a commit's SHA, or a branch named for a release.

### Using tags for release management

We recommend using tags for actions release management. Using this approach, your users can easily distinguish between major and minor versions:

- Erstellen und überprüfen Sie eine Version auf einem Release-Zweig (z. B. `release/v1`), bevor Sie das Release-Tag erstellen (z. B. `v1.0.2`).
- Erstellen Sie eine Version mit semantischer Versionierung. Weitere Informationen finden Sie unter „[Veröffentlichungen erstellen](/articles/creating-releases)“.
- Verschieben Sie das Hauptversions-Tag (z. B. `v1`, `v2`), um auf die Git-Ref der aktuellen Version zu verweisen. Weitere Informationen findest Du unter „[Git-Grundlagen - Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)“.
- Führen Sie ein neues Hauptversions-Tag (`v2`) für Änderungen ein, die vorhandene Workflows unterbrechen. Eine störende Änderung liegt beispielsweise vor, wenn die Eingabe einer Aktion geändert wird.
- Hauptversionen können zunächst mit einem `Beta-` -Tag veröffentlicht werden, um ihren Status anzugeben, z. B. `v2-beta`. Das `-beta-` -Tag kann dann entfernt werden, wenn es fertig ist.

This example demonstrates how a user can reference a major release tag:

```yaml
Schritte:
    - verwendet: actions/javascript-action@v1
```

This example demonstrates how a user can reference a specific patch release tag:

```yaml
Schritte:
    - verwendet: actions/javascript-action@v1.0.1
```

### Using branches for release management

If you prefer to use branch names for release management, this example demonstrates how to reference a named branch:

```yaml
Schritte:
    - verwendet: actions/javascript-action@v1-beta
```

### Using a commit's SHA for release management

Each Git commit receives a calculated SHA value, which is unique and immutable. Your action's users might prefer to rely on a commit's SHA value, as this approach can be more reliable than specifying a tag, which could be deleted or moved. However, this means that users will not receive further updates made to the action. {% ifversion fpt or ghes > 3.0 or ghae or ghec %}You must use a commit's full SHA value, and not an abbreviated value.{% else %}Using a commit's full SHA value instead of the abbreviated value can help prevent people from using a malicious commit that uses the same abbreviation.{% endif %}

```yaml
Schritte:
    - verwendet: actions/javascript-action@172239021f7ba04fe7327647b213799853a9eb89
```

## Eine README-Datei für die Aktion erstellen

Wenn Du Deine Aktion öffentlich bereitstellen möchten, empfehlen wir, eine README-Datei zu erstellen, damit andere Benutzer verstehen, wie die Aktion zu verwenden ist. Du kannst die folgenden Informationen in Ihre `README.md`-Datei aufnehmen:

- eine ausführliche Beschreibung, was die Aktion bewirkt
- erforderliche Eingabe- und Ausgabeargumente
- optionale Eingabe- und Ausgabeargumente
- Geheimnisse, die in der Aktion verwendet werden
- Umgebungsvariablen, die in der Aktion verwendet werden
- ein Beispiel für die Verwendung der Aktion in einem Workflow

## Unterschiede zwischen {% data variables.product.prodname_actions %} und {% data variables.product.prodname_github_apps %}

{% data variables.product.prodname_marketplace %} bietet Tools, um Deinen Workflow zu verbessern. Wenn Du die Unterschiede und die Vorteile der einzelnen Tools verstehst, kannst Du das beste Tool für Deinen Auftrag auswählen. For more information about building apps, see "[About apps](/apps/about-apps/)."

### Stärken von GitHub Aktionen und GitHub Apps

While both {% data variables.product.prodname_actions %} and {% data variables.product.prodname_github_apps %} provide ways to build automation and workflow tools, they each have strengths that make them useful in different ways.

{% data variables.product.prodname_github_apps %}:
* Laufen dauerhaft und können schnell auf Ereignisse reagieren.
* Funktionieren hervorragend, wenn persistente Daten benötigt werden.
* Funktionieren am besten mit API-Anforderungen, die nicht zeitaufwändig sind.
* Laufen auf Deinem Server oder auf Deiner Rechner-Infrastruktur.

{% data variables.product.prodname_actions %}:
* Bieten Automatisierung für eine kontinuierliche Integration und kontinuierliche Bereitstellung.
* Können direkt auf Runner-Maschinen oder in Docker-Containern laufen.
* Können auch Zugriff auf einen Clone Ihres Repositorys einschließen und dadurch Bereitstellungs- und Veröffentlichungs-Tools, Code-Formatierer und Befehlszeilen-Tools den Zugriff auf Ihren Code erlauben.
* Erfordern weder, dass Du Code noch eine App bereitstellst.
* Verfügen Sie über eine einfache Schnittstelle zum Erstellen und Verwenden von Geheimnissen. Dadurch können die Aktionen mit Diensten von Drittanbietern interagieren, ohne die Anmelde-Informationen des Aktions-Benutzers speichern zu müssen.

## Weiterführende Informationen

- „[Entwicklungstools für {% data variables.product.prodname_actions %}](/articles/development-tools-for-github-actions)“
