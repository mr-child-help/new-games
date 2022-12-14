---
title: About GitHub-hosted runners
intro: '{% data variables.product.prodname_dotcom %} bietet gehostete virtuelle Maschinen, um Workflows auszuführen. Die virtuelle Maschine umfasst eine Umgebung mit Tools, Paketen und Einstellungen für {% data variables.product.prodname_actions %}.'
redirect_from:
  - /articles/virtual-environments-for-github-actions
  - /github/automating-your-workflow-with-github-actions/virtual-environments-for-github-actions
  - /github/automating-your-workflow-with-github-actions/virtual-environments-for-github-hosted-runners
  - /actions/automating-your-workflow-with-github-actions/virtual-environments-for-github-hosted-runners
  - /actions/reference/virtual-environments-for-github-hosted-runners
  - /actions/reference/software-installed-on-github-hosted-runners
  - /actions/reference/specifications-for-github-hosted-runners
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
shortTitle: GitHub-hosted runners
---

{% data reusables.actions.ae-hosted-runners-beta %}
{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

## Informationen zu {% data variables.product.prodname_dotcom %}-gehosteten Runnern

Ein {% data variables.product.prodname_dotcom %}-gehosteter Runner ist eine virtuelle Maschine, die von {% data variables.product.prodname_dotcom %} gehostet wird und auf der die Runner-Anwendung der {% data variables.product.prodname_actions %} installiert ist. {% data variables.product.prodname_dotcom %} bietet Runner mit den Betriebssystemen Linux, Windows und MacOS.

Wenn Du einen {% data variables.product.prodname_dotcom %}-gehosteten Runner verwendest, werden Wartung und Upgrade der Maschine für Dich erledigt. Sie können Workflows direkt auf der virtuellen Maschine oder in einem Docker-Container ausführen.

Du kannst in einem Workflow für jeden Job die Art des Runners festlegen. Jeder Job in einem Workflow wird in einer neuen Instanz der virtuellen Maschine ausgeführt. Alle Schritte des Jobs werden in derselben Instanz der virtuellen Maschine ausgeführt, sodass die Aktionen in diesem Job über das Dateisystem Informationen austauschen können.

{% data reusables.github-actions.runner-app-open-source %}

### Cloud-Hosts für {% data variables.product.prodname_dotcom %}-gehostete Runner

{% data variables.product.prodname_dotcom %} betreibt Linux- und Windows-Runner auf den virtuellen Maschinen nach Standard_DS2_v2 in Microsoft Azure, auf denen die Runner-Anwendung der {% data variables.product.prodname_actions %} installiert ist. Die Runner-Anwendung auf {% data variables.product.prodname_dotcom %}-gehosteten Runnern ist eine Fork-Kopie des Azure-Pipelines-Agenten. Bei Azure werden eingehende ICMP-Pakete werden für alle virtuellen Maschinen blockiert, so dass die Befehle ping und traceroute möglicherweise nicht funktionieren. Weitere Informationen zu den Ressourcen der Standard_DS2_v2-Maschinen findest Du unter „[Serien Dv2 und DSv2](https://docs.microsoft.com/azure/virtual-machines/dv2-dsv2-series#dsv2-series)“ in der Dokumentation zu Microsoft Azure.

{% data variables.product.prodname_dotcom %} hosts macOS runners in {% data variables.product.prodname_dotcom %}'s own macOS Cloud.

### Workflow continuity for {% data variables.product.prodname_dotcom %}-hosted runners

{% data reusables.github-actions.runner-workflow-continuity %}

In addition, if the workflow run has been successfully queued, but has not been processed by a {% data variables.product.prodname_dotcom %}-hosted runner within 45 minutes, then the queued workflow run is discarded.

### Administrative Rechte von {% data variables.product.prodname_dotcom %}-gehosteten Runnern

Die virtuellen Maschinen unter Linux und macOS werden beide mit dem passwortlosen Befehl `sudo` ausgeführt. Wenn Sie Befehle ausführen oder Tools installieren müssen, die höhere Berechtigungen als der aktuelle Benutzer erfordern, können Sie `sudo` verwenden, ohne ein Passwort angeben zu müssen. Weitere Informationen findest Du im „[Sudo-Handbuch](https://www.sudo.ws/man/1.8.27/sudo.man.html)“.

Die virtuellen Windows-Maschinen sind so konfiguriert, dass sie als Administratoren laufen, wobei die Benutzerkonten-Steuerung (UAC) deaktiviert ist. For more information, see "[How User Account Control works](https://docs.microsoft.com/windows/security/identity-protection/user-account-control/how-user-account-control-works)" in the Windows documentation.

## Unterstützte Runner und Hardwareressourcen

Hardware specification for Windows and Linux virtual machines:
- CPU mit 2 Kernen
- 7 GB RAM-Speicher
- 14 GB SSD-Festplattenspeicher

Hardware specification for macOS virtual machines:
- CPU mit 3 Kernen
- 14 GB RAM-Speicher
- 14 GB SSD-Festplattenspeicher

{% data reusables.github-actions.supported-github-runners %}

Workflow logs list the runner used to run a job. For more information, see "[Viewing workflow run history](/actions/managing-workflow-runs/viewing-workflow-run-history)."

## Supported software

The software tools included in {% data variables.product.prodname_dotcom %}-hosted runners are updated weekly. The update process takes several days, and the list of preinstalled software on the `main` branch is updated after the whole deployment ends.
### Preinstalled software

Workflow logs include a link to the preinstalled tools on the exact runner. To find this information in the workflow log, expand the `Set up job` section. Under that section, expand the `Virtual Environment` section. The link following `Included Software` will describe the preinstalled tools on the runner that ran the workflow. ![Installed software link](/assets/images/actions-runner-installed-software-link.png) For more information, see "[Viewing workflow run history](/actions/managing-workflow-runs/viewing-workflow-run-history)."

For the overall list of included tools for each runner operating system, see the links below:

* [Ubuntu 20.04 LTS](https://github.com/actions/virtual-environments/blob/main/images/linux/Ubuntu2004-README.md)
* [Ubuntu 18.04 LTS](https://github.com/actions/virtual-environments/blob/main/images/linux/Ubuntu1804-README.md)
* [Windows Server 2022](https://github.com/actions/virtual-environments/blob/main/images/win/Windows2022-Readme.md)
* [Windows Server 2019](https://github.com/actions/virtual-environments/blob/main/images/win/Windows2019-Readme.md)
* [Windows Server 2016](https://github.com/actions/virtual-environments/blob/main/images/win/Windows2016-Readme.md)
* [macOS 11](https://github.com/actions/virtual-environments/blob/main/images/macos/macos-11-Readme.md)
* [macOS 10.15](https://github.com/actions/virtual-environments/blob/main/images/macos/macos-10.15-Readme.md)

{% data variables.product.prodname_dotcom %}-gehostete Runner enthalten zusätzlich zu den oben aufgeführten Paketen die standardmäßig integrierten Tools des Betriebssystems. Zum Beispiel beinhalten Ubuntu und macOS Läufer `grep`, `find`, und `which` neben anderen Standard-Tools.

### Using preinstalled software

We recommend using actions to interact with the software installed on runners. This approach has several benefits:
- Usually, actions provide more flexible functionality like versions selection, ability to pass arguments, and parameters
- It ensures the tool versions used in your workflow will remain the same regardless of software updates

Wenn Sie ein bestimmtes Tool anfordern möchten, öffnen Sie bitte einen Issue unter [actions/virtual-environments](https://github.com/actions/virtual-environments). This repository also contains announcements about all major software updates on runners.

### Installing additional software

You can install additional software on {% data variables.product.prodname_dotcom %}-hosted runners. For more information, see "[Customizing GitHub-hosted runners](/actions/using-github-hosted-runners/customizing-github-hosted-runners)".

## IP addresses

{% note %}

**Notiz:** Wenn Du eine Liste mit erlaubten IP-Adressen für Dein Organisations- oder Unternehmenskonto auf {% data variables.product.prodname_dotcom %} verwendest, kannst Du keine {% data variables.product.prodname_dotcom %}-gehosteten Runner verwenden, sondern benötigst stattdessen selbst-gehostete Runner. Weitere Informationen findest Du unter „[Informationen zu selbst-gehosteten Runnern](/actions/hosting-your-own-runners/about-self-hosted-runners)“.

{% endnote %}

Windows and Ubuntu runners are hosted in Azure and subsequently have the same IP address ranges as the Azure datacenters. macOS runners are hosted in {% data variables.product.prodname_dotcom %}'s own macOS cloud.

To get a list of IP address ranges that {% data variables.product.prodname_actions %} uses for {% data variables.product.prodname_dotcom %}-hosted runners, you can use the {% data variables.product.prodname_dotcom %} REST API . For more information, see the `actions` key in the response of the "[Get GitHub meta information](/rest/reference/meta#get-github-meta-information)" endpoint. You can use this list of IP addresses if you require an allow-list to prevent unauthorized access to your internal resources.

The list of {% data variables.product.prodname_actions %} IP addresses returned by the API is updated once a week.

## File systems

{% data variables.product.prodname_dotcom %} führt Aktionen und Shell-Befehle in bestimmten Verzeichnissen auf der virtuellen Maschine aus. Die Dateipfade auf virtuellen Maschinen sind nicht statisch. Verwende die von {% data variables.product.prodname_dotcom %} bereitgestellten Umgebungsvariablen zum Erstellen von Dateipfaden für die Verzeichnisse `home`, `workspace`und `workflow`.

| Verzeichnis           | Umgebungsvariable   | Beschreibung                                                                                                                                                                                                                           |
| --------------------- | ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `home`                | `HOME`              | Enthält benutzerbezogene Daten. In diesem Verzeichnis können sich beispielsweise die Anmeldeinformation aus einem Anmeldeversuch befinden.                                                                                             |
| `workspace`           | `GITHUB_WORKSPACE`  | Aktionen und Shell-Befehle werden in diesem Verzeichnis ausgeführt. Eine Aktion kann den Inhalt dieses Verzeichnisses ändern, auf den dann nachfolgende Aktionen zugreifen können.                                                     |
| `workflow/event.json` | `GITHUB_EVENT_PATH` | Die `POST`-Nutzlast des Webhook-Ereignisses, das den Workflow ausgelöst hat. {% data variables.product.prodname_dotcom %} schreibt dies bei jeder ausgeführten Aktion neu, sodass der Dateiinhalt zwischen den Aktionen isoliert wird. |

Eine Liste der von {% data variables.product.prodname_dotcom %} für jeden Workflow erstellten Umgebungsvariablen findest Du unter „[Umgebungsvariablen verwenden](/github/automating-your-workflow-with-github-actions/using-environment-variables)“.

### Docker-Container-Dateisystem

Für Aktionen, die in Docker-Containern ausgeführt werden, befinden sich statische Verzeichnisse im Pfad `/github`. Wir empfehlen jedoch dringend, die Standard-Umgebungsvariablen zu verwenden, um Dateipfade in Docker-Containern zu erstellen.

In {% data variables.product.prodname_dotcom %} wird das Pfadpräfix `/github` reserviert, und es werden drei Verzeichnisse für Aktionen erstellt.

- `/github/home`
- `/github/workspace` - {% data reusables.repositories.action-root-user-required %}
- `/github/workflow`

{% ifversion fpt or ghec %}

## Weiterführende Informationen
- "[ Abrechnung für {% data variables.product.prodname_actions %} verwalten](/billing/managing-billing-for-github-actions)"

{% endif %}
