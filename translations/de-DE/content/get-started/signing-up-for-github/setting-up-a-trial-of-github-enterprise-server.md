---
title: Eine Testversion von GitHub Enterprise Server einrichten
intro: 'Sie können {% data variables.product.prodname_ghe_server %} kostenlos testen.'
redirect_from:
  - /articles/requesting-a-trial-of-github-enterprise/
  - /articles/setting-up-a-trial-of-github-enterprise-server
  - /github/getting-started-with-github/setting-up-a-trial-of-github-enterprise-server
  - /github/getting-started-with-github/signing-up-for-github/setting-up-a-trial-of-github-enterprise-server
versions:
  fpt: '*'
  ghec: '*'
  ghes: '*'
topics:
  - Accounts
shortTitle: Enterprise Server trial
---

## Informationen zu {% data variables.product.prodname_ghe_server %}-Testversionen

Sie können eine Testversion anfordern und {% data variables.product.prodname_ghe_server %} 45 Tage lang kostenlos testen. Deine Testversion wird als virtuelle Appliance installiert, wobei Du wählen kannst, ob sie lokal oder in der Cloud bereitgestellt wird. Eine Liste der unterstützten Visualisierungsplattformen findest Du unter „[GitHub Enterprise Server-Instanz einrichten](/enterprise-server@latest/admin/installation/setting-up-a-github-enterprise-server-instance).“

{% ifversion ghes %}{% data variables.product.prodname_dependabot %}{% else %}Security{% endif %} alerts and {% data variables.product.prodname_github_connect %} are not currently available in trials of {% data variables.product.prodname_ghe_server %}. Kontaktiere {% data variables.contact.contact_enterprise_sales %} für eine Vorstellung dieser Funktionen. For more information about these features, see "[About alerts for vulnerable dependencies](/github/managing-security-vulnerabilities/about-alerts-for-vulnerable-dependencies)" and "[Connecting your enterprise account to {% data variables.product.prodname_ghe_cloud %}](/enterprise-server@latest/admin/configuration/managing-connections-between-your-enterprise-accounts/connecting-your-enterprise-account-to-github-enterprise-cloud)."

Testversionen sind auch für {% data variables.product.prodname_ghe_cloud %} verfügbar. Weitere Informationen findest Du unter „[Eine Testversion von {% data variables.product.prodname_ghe_cloud %} einrichten](/articles/setting-up-a-trial-of-github-enterprise-cloud).“

{% data reusables.products.which-product-to-use %}

## Deine {% data variables.product.prodname_ghe_server %}-Testversion einrichten

{% data variables.product.prodname_ghe_server %} wird als virtuelle Appliance installiert. Wähle in Deiner Organisation die Person aus, die Du mit der Einrichtung einer virtuellen Maschine beauftragen möchtest, und bitte diese, eine [Testversion anzufordern](https://enterprise.github.com/trial). Mit dem Test kannst Du sofort nach dem Absenden der Anfrage beginnen.

Klicke zur Einrichtung eines Kontos für das {% data variables.product.prodname_enterprise %}-Webportal auf den Link in der E-Mail, die Du nach dem Anfordern Deiner Testversion erhalten hast, und folge den Eingabeaufforderungen. Lade anschließend Deine Lizenzdatei herunter. For more information, see "[Managing your license for {% data variables.product.prodname_enterprise %}](/enterprise-server@latest/billing/managing-your-license-for-github-enterprise)."

Lade zur Installation von {% data variables.product.prodname_ghe_server %} die erforderlichen Komponenten herunter, und lade Deine Lizenzdatei hoch. Weitere Informationen finden Sie in den Anweisungen zur gewählten Visualisierungsplattform unter „[{% data variables.product.prodname_ghe_server %}-Instanz einrichten](/enterprise-server@latest/admin/installation/setting-up-a-github-enterprise-server-instance)“.

## Nächste Schritte:

Um Deine Testversion optimal zu nutzen, folge diesen Schritten:

1. [Erstellen Sie eine Organisation](/enterprise-server@latest/admin/user-management/creating-organizations).
2. Die grundlegenden Schritte der Verwendung von {% data variables.product.prodname_dotcom %} werden unter folgenden Links beschrieben:
   - Webcast „[Kurzanleitung zu {% data variables.product.prodname_dotcom %}](https://resources.github.com/webcasts/Quick-start-guide-to-GitHub/)“
   - „[Verstehen des {% data variables.product.prodname_dotcom %}-Ablaufs](https://guides.github.com/introduction/flow/)“ unter „{% data variables.product.prodname_dotcom %}-Anleitungen“
   - „[Hello World](https://guides.github.com/activities/hello-world/)“ unter „{% data variables.product.prodname_dotcom %}-Anleitungen“
3. To configure your instance to meet your organization's needs, see "[Configuring your enterprise](/enterprise-server@latest/admin/configuration/configuring-your-enterprise)."
4. Integrieren Sie {% data variables.product.prodname_ghe_server %} mit Ihrem Identity Provider. Details finden Sie unter „[SAML verwenden](/enterprise-server@latest/admin/user-management/using-saml)“ und „[LDAP verwenden](/enterprise-server@latest/admin/authentication/using-ldap)“.
5. Lade beliebig viele Personen zum Test ein.
   - Füge die Benutzer zu Deiner {% data variables.product.prodname_ghe_server %}-Instanz hinzu, entweder mit der integrierten Authentifizierung oder Deinem konfigurierten Identitätsanbieter. Weitere Informationen finden Sie unter „[Integrierte Authentifizierung verwenden](/enterprise-server@latest/admin/user-management/using-built-in-authentication)“.
   - Wenn Du Personen als Kontoadministratoren einladen möchtest, besuche das [{% data variables.product.prodname_enterprise %}-Webportal](https://enterprise.github.com/login).

    {% note %}

    **Note:** People you invite to become account administrators will receive an email with a link to accept your invitation.

    {% endnote %}

{% data reusables.products.product-roadmap %}

## Test beenden

Im [{% data variables.product.prodname_enterprise %}-Webportal](https://enterprise.github.com/login) können Sie jederzeit während des Testzeitraums auf vollständige Lizenzen umstellen.

Wenn das Upgrade nicht spätestens am letzten Tag des Testzeitraums erfolgt, erhalten Sie eine E-Mail, die Sie über die Beendigung des Tests informiert. Wenn Du mehr Zeit für die Beurteilung von {% data variables.product.prodname_enterprise %} benötigst, kontaktiere bitte {% data variables.contact.contact_enterprise_sales %} für eine Verlängerung.

## Weiterführende Informationen

- „[Eine Testversion von {% data variables.product.prodname_ghe_cloud %} einrichten](/get-started/signing-up-for-github/setting-up-a-trial-of-github-enterprise-cloud)“
