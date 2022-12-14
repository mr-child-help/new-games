---
title: Issuevorlagen für Dein Repository konfigurieren
intro: 'Du kannst die Vorlagen anpassen, die für Mitarbeiter zur Verfügung stehen, wenn sie neue Issues in Deinem Repository eröffnen.'
redirect_from:
  - /github/building-a-strong-community/creating-issue-templates-for-your-repository
  - /articles/configuring-issue-templates-for-your-repository
  - /github/building-a-strong-community/configuring-issue-templates-for-your-repository
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Community
shortTitle: Configure
---

{% ifversion fpt or ghes or ghec %}

{% data reusables.repositories.default-issue-templates %}

{% endif %}

{% ifversion fpt or ghae or ghes or ghec %}

## Issuevorlagen erstellen

{% endif %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
3. Klicke im Abschnitt „Features“ (Funktionen) unter „Issues“ auf **Set up templates** (Vorlagen einrichten). ![Schaltfläche „Start template setup" (Starten der Vorlageneinrichtung)](/assets/images/help/repository/set-up-templates.png)
4. Klicke im Dropdownmenü „Add template“ (Vorlage hinzufügen) auf den gewünschten Vorlagentyp, den Du erstellen möchtest. ![Dropdownmenü „Add template“ (Vorlage hinzufügen)](/assets/images/help/repository/add-template-drop-down-menu.png)
5. Um eine Vorschau der Vorlage anzuzeigen oder die Vorlage zu bearbeiten, bevor Du sie an das Repository freigibst, klicke auf **Preview and edit** (Anzeigen und Bearbeiten). ![Schaltfläche „Preview and edit“ (anzeigen und bearbeiten)](/assets/images/help/repository/preview-and-edit-button.png)
6. Um die Vorlage zu bearbeiten, klicken Sie auf {% octicon "pencil" aria-label="The edit icon" %}, und ändern Sie die Inhalte der Felder. ![Schaltfläche „Issue template edit" (Bearbeiten der Issuevorlage)](/assets/images/help/repository/issue-template-edit-button.png)
7. Um automatisch einen standardmäßigen Issuetitel einzurichten, weise den Issue an Benutzern mit Lesezugriff auf das Repository zu. Du kannst auch Kennzeichnungen zur Issuevorlage hinzufügen und diese Details unter „Optional additional Information“ (Optionale zusätzliche Informationen) eingeben. Außerdem kannst Du diese Details auch in der Issuevorlage mit `title`, `labels` oder `assignees` im YAML-Titelei-Format hinzufügen. ![Zusätzliche Informationen für Issuevorlagen](/assets/images/help/repository/additional-issue-template-info.png)
8. Wenn mit der Vorschau und Bearbeitung der Vorlage fertig bist, klicke in der oberen rechten Ecke der Seite auf **Propose changes** (Änderungen vorschlagen). ![Schaltfläche „Propose changes“ (Änderungen vorschlagen)](/assets/images/help/repository/propose-changes-button.png)
9. Gib eine Commit-Mitteilung ein, in der Du Deine Änderungen beschreibst. ![Feld „Issue template commit message" (Commit-Mitteilung für Issuevorlage)](/assets/images/help/repository/issue-template-commit-message-field.png)
10. Lege unterhalb der Commit-Mitteilungsfelder fest, ob Du Deine Vorlage direkt an den Standardbranch freigeben oder einen neuen Branch erstellen und einen Pull Request öffnen möchtest. Weitere Informationen zu Pull Requests findest Du unter „[Informationen zu Pull Requests](/articles/about-pull-requests).“ ![Issue template commit to main or open pull request choice](/assets/images/help/repository/issue-template-commit-to-master-or-open-pull-request.png)
11. Klicke auf **Commit changes** (Änderungen freigeben). Sobald diese Änderungen in den Standardbranch zusammengeführt wurden, steht die Vorlage für Mitarbeiter zur Verfügung, wenn sie neue Issues im Repository erstellen.

{% ifversion fpt or ghec %}

## Creating issue forms

{% data reusables.community.issue-forms-beta %}

With issue forms, you can create issue templates that have customizable web form fields. You can encourage contributors to include specific, structured information by using issue forms in your repository. Issue forms are written in YAML using the {% data variables.product.prodname_dotcom %} form schema. For more information, see "[Syntax for {% data variables.product.prodname_dotcom %}'s form schema](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema)." {% data reusables.actions.learn-more-about-yaml %}

To use an issue form in your repository, you must create a new file and add it to the `.github/ISSUE_TEMPLATE` folder in your repository.

Here is an example of an issue form configuration file.

{% data reusables.community.issue-forms-sample %}

Here is the rendered version of the issue form. ![A rendered issue form](/assets/images/help/repository/sample-issue-form.png)

1. Choose a repository where you want to create an issue form. You can use an existing repository that you have write access to, or you can create a new repository. Weitere Informationen zum Erstellen eines Repositorys findest Du unter „[Ein neues Repository erstellen](/articles/creating-a-new-repository).“
2. In your repository, create a file called `.github/ISSUE_TEMPLATE/FORM-NAME.yml`, replacing `FORM-NAME` with the name for your issue form. For more information about creating new files on GitHub, see "[Creating new files](/github/managing-files-in-a-repository/creating-new-files)."
3. In the body of the new file, type the contents of your issue form. For more information, see "[Syntax for issue forms](/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-issue-forms)."
4. Commit your file to the default branch of your repository. Weitere Informationen finden Sie unter „[Neue Dateien erstellen](/github/managing-files-in-a-repository/creating-new-files)“.

{% endif %}

{% ifversion fpt or ghae or ghes or ghec %}
## Konfigurieren der Vorlagenauswahl

{% data reusables.repositories.issue-template-config %}

You can encourage contributors to use issue templates by setting `blank_issues_enabled` to `false`. Wenn Du `blank_issues_enabled` (leere Issues ermöglichen) auf `true` (gültig) setzt, haben Personen die Möglichkeit, leere Issues zu eröffnen.

{% note %}

**Note:** If you used the legacy workflow to manually create an `issue_template.md` file in the `.github` folder and enable blank issues in your *config.yml* file, the template in `issue_template.md` will be used when people chose to open a blank issue. Wenn Du leere Issues deaktivierst, wird diese Vorlage nie verwendet.

{% endnote %}

Wenn Du bestimmte Berichte außerhalb von {% data variables.product.product_name %} erhalten möchtest, kannst Du Personen mit `contact_links` auf externe Websites leiten.

Hier ist ein Beispiel für die *config.yml*-Datei.

```shell
blank_issues_enabled: false
contact_links:
  - name: {% data variables.product.prodname_gcf %}
    url: https://github.community/
    about: Please ask and answer questions here.
  - name: {% data variables.product.prodname_dotcom %} Security Bug Bounty
    url: https://bounty.github.com/
    about: Please report security vulnerabilities here.
```

Deine Konfigurationsdatei wird die Vorlagenauswahl anpassen, wenn die Datei in den Standardbranch des Repository zusammengeführt wird.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.files.add-file %}
3. Gib im Feld Dateiname `.github/ISSUE_TEMPLATE/config.yml` ein. ![Konfigurationsdateiname](/assets/images/help/repository/template-config-file-name.png)
4. Gib im Textfeld der neuen Datei den Inhalt Deiner Konfigurationsdatei ein. ![Inhalt der Konfigurationsdatei](/assets/images/help/repository/template-config-file-content.png)
{% data reusables.files.write_commit_message %}
{% data reusables.files.choose_commit_branch %}
{% data reusables.files.propose_new_file %}
{% endif %}

## Weiterführende Informationen

- „[Informationen zu Vorlagen für Issues und Pull-Requests](/articles/about-issue-and-pull-request-templates)“
- „[Eine einzelne Issue-Vorlage für Dein Repository manuell erstellen](/articles/manually-creating-a-single-issue-template-for-your-repository)“
