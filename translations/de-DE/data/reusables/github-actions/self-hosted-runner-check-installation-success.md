
### Überprüfung dass Dein selbst-gehosteter Läufer erfolgreich hinzugefügt wurde

After completing the steps to add a self-hosted runner, the runner and its status are now listed under {% ifversion fpt or ghec %}"Runners"{% elsif ghae or ghes %}"Self-hosted runners"{% endif %}.

Die selbst-gehostete Läuferanwendung muss aktiv sein, damit der Läufer Aufträge annehmen kann. Wenn die Läuferanwendung mit {% data variables.product.product_name %} verbunden und bereit ist, Aufträge zu empfangen, siehst Du die folgende Meldung auf dem Terminal der Maschine.

{% data reusables.github-actions.self-hosted-runner-connected-output %}

Weitere Informationen findest Du unter "[Überwachung und Fehlerbehebung selbst-gehosteter Läufer ](/actions/hosting-your-own-runners/monitoring-and-troubleshooting-self-hosted-runners)."
