---
title: Eine Veröffentlichungsquelle für Deine GitHub Pages-Website konfigurieren
intro: 'Wenn Sie die Standard-Veröffentlichungsquelle für Ihre {% data variables.product.prodname_pages %}-Website verwenden, wird Ihre Website automatisch veröffentlicht. You can also choose to publish your site from a different branch or folder.'
redirect_from:
  - /articles/configuring-a-publishing-source-for-github-pages/
  - /articles/configuring-a-publishing-source-for-your-github-pages-site
  - /github/working-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
product: '{% data reusables.gated-features.pages %}'
permissions: 'People with admin or maintainer permissions for a repository can configure a publishing source for a {% data variables.product.prodname_pages %} site.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Pages
shortTitle: Configure publishing source
---

Weitere Informationen zu Veröffentlichungsquellen findest Du unter „[Informationen zu {% data variables.product.prodname_pages %}](/articles/about-github-pages#publishing-sources-for-github-pages-sites).“

## Eine Veröffentlichungsquelle auswählen

Before you configure a publishing source, make sure the branch you want to use as your publishing source already exists in your repository.

{% data reusables.pages.navigate-site-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.pages.sidebar-pages %}
3. Under "{% data variables.product.prodname_pages %}", use the **None** or **Branch** drop-down menu and select a publishing source. ![Drop-down menu to select a publishing source](/assets/images/help/pages/publishing-source-drop-down.png)
4. Optionally, use the drop-down menu to select a folder for your publishing source. ![Drop-down menu to select a folder for publishing source](/assets/images/help/pages/publishing-source-folder-drop-down.png)
5. Klicke auf **Save** (Speichern). ![Button to save changes to publishing source settings](/assets/images/help/pages/publishing-source-save.png)

## Fehler bei der Veröffentlichung Deiner {% data variables.product.prodname_pages %}-Website beheben

{% data reusables.pages.admin-must-push %}

If you choose the `docs` folder on any branch as your publishing source, then later remove the `/docs` folder from that branch in your repository, your site won't build and you'll get a page build error message for a missing `/docs` folder. Weitere Informationen findest Du unter „[Jekyll-Build-Fehler für {% data variables.product.prodname_pages %}-Websites beheben](/articles/troubleshooting-jekyll-build-errors-for-github-pages-sites#missing-docs-folder).“
