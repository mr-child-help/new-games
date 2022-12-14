---
title: Creating a GitHub Pages site
intro: 'Sie können eine {% data variables.product.prodname_pages %}-Website in einem neuen oder vorhandenen Repository erstellen.'
redirect_from:
  - /articles/creating-pages-manually/
  - /articles/creating-project-pages-manually/
  - /articles/creating-project-pages-from-the-command-line/
  - /articles/creating-project-pages-using-the-command-line/
  - /articles/creating-a-github-pages-site
  - /github/working-with-github-pages/creating-a-github-pages-site
product: '{% data reusables.gated-features.pages %}'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pages
shortTitle: Create a GitHub Pages site
---

{% data reusables.pages.org-owners-can-restrict-pages-creation %}

## Ein Repository für eine Website erstellen

{% data reusables.pages.new-or-existing-repo %}

{% data reusables.repositories.create_new %}
{% data reusables.repositories.owner-drop-down %}
{% data reusables.pages.create-repo-name %}
{% data reusables.repositories.choose-repo-visibility %}
{% data reusables.repositories.initialize-with-readme %}
{% data reusables.repositories.create-repo %}

## Eine Website erstellen

{% data reusables.pages.must-have-repo-first %}

{% data reusables.pages.private_pages_are_public_warning %}

{% data reusables.pages.navigate-site-repo %}
{% data reusables.pages.decide-publishing-source %}
3. Wenn Deine ausgewählte Veröffentlichungsquelle bereits vorhanden ist, navigiere zu dieser Quelle. Wenn Deine ausgewählte Veröffentlichungsquelle nicht vorhanden ist, erstelle die Veröffentlichungsquelle.
4. Erstelle im Root der Veröffentlichungsquelle eine neue Datei mit dem Namen `index.md`, die den Inhalt enthält, der auf der Hauptseite Deiner Website angezeigt werden soll.

  {% tip %}

  **Tip:** If `index.html` is present, this will be used instead of `index.md`. If neither `index.html` nor `index.md` are present, `README.md` will be used.

  {% endtip %}
{% data reusables.pages.configure-publishing-source %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.pages.sidebar-pages %}{% ifversion fpt or ghec %}
{% data reusables.pages.choose-visibility %}{% endif %}
{% data reusables.pages.visit-site %}

{% data reusables.pages.admin-must-push %}

## Nächste Schritte:

Du kannst Deiner Website weitere Seiten hinzufügen, indem Du zusätzliche neue Dateien erstellst. Jede Datei wird auf Deiner Website im selben Verzeichnis verfügbar sein wie Deine Veröffentlichungsquelle. Wenn beispielsweise die Veröffentlichungsquelle für Deine Projekt-Website der Branch `gh-pages` ist und Du eine neue Datei mit dem Namen `/about/contact-us.md` auf dem Branch `gh-pages` erstellst, ist die Datei unter {% ifversion fpt or ghec %}`https://<user>.github.io/<repository>/{% else %}`http(s)://<hostname>/pages/<username>/<repository>/{% endif %}about/contact-us.html` verfügbar.

Du kannst auch ein Design hinzufügen, um das Aussehen der Website anzupassen. Weitere Informationen findest Du unter {% ifversion fpt or ghec %}„[Ein Design mit dem Theme Chooser zu Deiner {% data variables.product.prodname_pages %}-Website hinzufügen](/articles/adding-a-theme-to-your-github-pages-site-with-the-theme-chooser){% else %}„[Ein Design zu Deiner {% data variables.product.prodname_pages %}-Website mit Jekyll hinzufügen](/articles/adding-a-theme-to-your-github-pages-site-using-jekyll){% endif %}.“

Um Ihre Website noch weiter anzupassen, können Sie Jekyll verwenden, einen Generator für statische Websites mit integrierter Unterstützung von {% data variables.product.prodname_pages %}. Weitere Informationen finden Sie unter „[Informationen zu {% data variables.product.prodname_pages %} und Jekyll](/articles/about-github-pages-and-jekyll)“.

## Weiterführende Informationen

- „[Jekyll-Build-Fehler für {% data variables.product.prodname_pages %}-Websites beheben](/articles/troubleshooting-jekyll-build-errors-for-github-pages-sites)“
- „[Branches in Ihrem Repository erstellen und löschen](/articles/creating-and-deleting-branches-within-your-repository)“
- „[Neue Dateien erstellen](/articles/creating-new-files)“
