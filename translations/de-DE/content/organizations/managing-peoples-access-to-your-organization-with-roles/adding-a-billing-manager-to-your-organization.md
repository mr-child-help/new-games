---
title: Abrechnungsmanager zu Deine Organisation hinzufügen
intro: 'Ein *Abrechnungsmanager* ist ein Benutzer, der die Abrechnungseinstellungen für Deine Organisation verwaltet. Er aktualisiert beispielsweise die Zahlungsinformationen. Es ist eine hilfreiche Option, wenn normale Mitglieder Deiner Organisation typischerweise keinen Zugriff auf Abrechnungsressourcen haben.'
redirect_from:
  - /articles/adding-a-billing-manager-to-your-organization
  - /github/setting-up-and-managing-organizations-and-teams/adding-a-billing-manager-to-your-organization
versions:
  fpt: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
  - Billing
shortTitle: Add a billing manager
---

Mitglieder vom Team des Inhabers Deiner Organisation können anderen Benutzern *Abrechnungsmanager*-Berechtigungen zuweisen. Wenn ein Benutzer die Einladung, Abrechnungsmanager zu werden, annimmt, kann er weitere Benutzer einladen, Abrechnungsmanager zu werden.

{% note %}

**Hinweis:** Abrechnungsmanager nutzen keine bezahlte Lizenz im Abonnement Deiner Organisation.

{% endnote %}

## Berechtigungen für Abrechnungsmanager

Abrechnungsmanager können

- Das Konto herauf- oder herabstufen,
- Zahlungsmethoden hinzufügen, aktualisieren oder entfernen,
- Den Zahlungsverlauf anzeigen,
- Quittungen herunterladen,
- Abrechnungsmanager anzeigen, einladen und entfernen.
- Start, modify, or cancel sponsorships

Zusätzlich erhalten alle Abrechnungsmanager am Abrechnungsdatum der Organisation per E-Mail Abrechnungsquittungen.

Abrechnungsmanager können **nicht**

- Repositorys in Deinen Organisationen erstellen oder auf sie zugreifen,
- Die privaten Mitglieder Deiner Organisation sehen,
- In der Liste der Mitglieder der Organisation gesehen werden,
- Abonnements für {% data variables.product.prodname_marketplace %}-Apps erwerben, bearbeiten oder stornieren.

{% tip %}

**Tipp:** Wenn Deine Organisation [die Zwei-Faktor-Authentifizierung für Mitglieder, Abrechnungsmanager und externe Mitarbeiter vorschreibt](/articles/requiring-two-factor-authentication-in-your-organization), muss der Benutzer die Zwei-Faktor-Authentifizierung aktivieren, bevor er Deine Einladung, Abrechnungsmanager für die Organisation zu werden, annehmen kann.

{% endtip %}

## Abrechnungsmanager einladen

{% ifversion ghec %}
{% note %}

**Note:** If your organization is managed using [Enterprise Accounts](/github/setting-up-and-managing-your-enterprise/managing-your-enterprise-account/about-enterprise-accounts) you will not be able to invite Billing Managers at the organization level.

{% endnote %}
{% endif %}

Der eingeladene Benutzer erhält eine Einladungs-E-Mail, in der er darum gebeten wird, Abrechnungsmanager für Deine Organisation zu werden. Wenn der eingeladene Benutzer in der E-Mail auf den Link zum Annehmen der Einladung klickt, wird er automatisch als Abrechnungsmanager zur Organisation hinzugefügt. Wenn er noch kein GitHub-Konto besitzt, wird er auf eine Seite umgeleitet, auf der er ein Konto erstellen kann. Nach der Erstellung des Kontos wird er automatisch als Abrechnungsmanager zur Organisation hinzugefügt.

{% data reusables.organizations.billing-settings %}
1. Under "Billing management", next to "Billing managers", click **Add**. ![Abrechnungsmanager einladen](/assets/images/help/billing/settings_billing_managers_list.png)
6. Gib den Benutzernamen oder die E-Mail-Adresse des Benutzers ein, den Du hinzufügen möchtest, und klicke auf **Send invitation** (Einladung versenden). ![Seite zum Einladen eines Abrechnungsmanagers](/assets/images/help/billing/billing_manager_invite.png)
