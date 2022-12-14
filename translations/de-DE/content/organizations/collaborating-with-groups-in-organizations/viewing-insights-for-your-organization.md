---
title: Organisationseinblicke anzeigen
intro: 'Organisationseinblicke enthalten Daten zu den Aktivitäten, Beiträgen und Abhängigkeiten Deiner Organisation.'
product: '{% data reusables.gated-features.org-insights %}'
redirect_from:
  - /articles/viewing-insights-for-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/viewing-insights-for-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: View organization insights
---

Alle Mitglieder einer Organisation können Organisationseinblicke anzeigen. For more information, see "[Roles in an organization](/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization)."

Mithilfe von Einblicken in Organisationsaktivitäten kannst Du besser nachvollziehen, wie die Mitglieder Deiner Organisation {% data variables.product.product_name %} verwenden, um zusammenzuarbeiten und Code zu erstellen. Mithilfe von Abhängigkeits-Einblicken kannst Du die Open-Source-Nutzung Deiner Organisation nachverfolgen, melden und entsprechend darauf reagieren.

## Einblicke in Organisationsaktivitäten anzeigen

{% note %}

**Hinweis:** Einblicke in Organisationsaktivitäten liegen derzeit als Beta-Funktion vor und können sich jederzeit verändern.

{% endnote %}

Mithilfe von Einblicken in Organisationsaktivitäten kannst Du wöchentliche, monatliche und jährliche Datenvisualisierungen Deiner gesamten Organisation oder von spezifischen Repositorys anzeigen. Dazu zählen Issue- und Pull-Request-Aktivitäten, die am häufigsten verwendeten Sprachen sowie kumulative Informationen dahingehend, wo Deine Organisationsmitglieder ihre Zeit aufgewendet haben.

{% data reusables.profile.access_org %}
{% data reusables.user_settings.access_org %}
3. Klicke unter dem Namen Deiner Organisation auf {% octicon "graph" aria-label="The bar graph icon" %} **Insights** (Einblicke). ![Klicke auf die Registerkarte „Insights“ (Einblicke) der Organisation](/assets/images/help/organizations/org-nav-insights-tab.png)
4. Wähle optional in der oberen rechten Ecke der Seite die entsprechende Option aus, um Daten für die letzte **1 Woche**, **1 Monat** oder **1 Jahr** anzuzeigen. ![Auswahl des Zeitraums zum Anzeigen der Organisationseinblicke](/assets/images/help/organizations/org-insights-time-period.png)
5. Wähle optional in der oberen rechten Ecke der Seite die entsprechende Option aus, um Daten für bis zu drei Repositorys anzuzeigen, und klicke auf **Apply** (Anwenden). ![Auswahl von Repositorys zum Anzeigen der Organisationseinblicke](/assets/images/help/organizations/org-insights-repos.png)

## Organisations-Abhängigkeits-Einblicke anzeigen

{% note %}

**Note:** Please make sure you have enabled the [Dependency Graph](/code-security/supply-chain-security/understanding-your-software-supply-chain/about-the-dependency-graph#enabling-the-dependency-graph).

{% endnote %}

Mithilfe von Abhängigkeits-Einblicken kannst Du Schwachstellen, Lizenzen und andere wichtige Informationen für die Open-Source-Projekte anzeigen, von denen Deine Organisation abhängig ist.

{% data reusables.profile.access_org %}
{% data reusables.user_settings.access_org %}
3. Klicke unter dem Namen Deiner Organisation auf {% octicon "graph" aria-label="The bar graph icon" %} **Insights** (Einblicke). ![Registerkarte „Insights“ (Einblicke) auf der Haupt-Navigationsleiste der Organisation](/assets/images/help/organizations/org-nav-insights-tab.png)
4. Klicke zum Anzeigen von Abhängigkeiten für diese Organisation auf **Dependencies** (Abhängigkeiten). ![Registerkarte „Dependencies“ (Abhängigkeiten) unter der Haupt-Navigationsleiste der Organisation](/assets/images/help/organizations/org-insights-dependencies-tab.png)
5. Klicke zum Anzeigen von Abhängigkeits-Einblicken für alle Deine {% data variables.product.prodname_ghe_cloud %}-Organisationen auf **My organizations** (Meine Organisationen). ![Schaltfläche „My organizations“ (Meine Organisationen) unter der Registerkarte „Dependencies“ (Abhängigkeiten)](/assets/images/help/organizations/org-insights-dependencies-my-orgs-button.png)
6. Du kannst auf die Ergebnisse in den Diagrammen **Open security advisories** (Offene Sicherheitshinweise) und **Licenses** (Lizenzen) klicken, um nach einem Schwachstellenstatus, nach einer Lizenz oder nach einer Kombination aus beiden zu filtern. ![My organizations vulnerabilities and licenses graphs](/assets/images/help/organizations/org-insights-dependencies-graphs.png)
7. Neben der jeweiligen Schwachstelle können Sie auf {% octicon "package" aria-label="The package icon" %} **dependents** (Abhängige) klicken, um nachzuvollziehen, welche Abhängigen in Ihrer Organisation jede Bibliothek verwenden. ![Angreifbare Abhängige der eigenen Organisationen](/assets/images/help/organizations/org-insights-dependencies-vulnerable-item.png)

## Weiterführende Informationen
 - „[Informationen zu Organisationen](/organizations/collaborating-with-groups-in-organizations/about-organizations)“
 - "[Exploring the dependencies of a repository](/github/visualizing-repository-data-with-graphs/exploring-the-dependencies-of-a-repository)"
 - "[Changing the visibility of your organization's dependency insights](/organizations/managing-organization-settings/changing-the-visibility-of-your-organizations-dependency-insights)"{% ifversion ghec %}
- "[Enforcing policies for dependency insights in your enterprise](/admin/policies/enforcing-policies-for-your-enterprise/enforcing-policies-for-dependency-insights-in-your-enterprise)"{% endif %}
