---
title: Code durchsuchen
intro: 'Auf {% data variables.product.product_name %} können Sie Code durchsuchen und die Suchergebnisse mit den folgenden Kennzeichnern der Codesuche in beliebiger Kombination eingrenzen.'
redirect_from:
  - /articles/searching-code
  - /github/searching-for-information-on-github/searching-files-in-a-repository-for-exact-matches
  - /github/searching-for-information-on-github/searching-code-for-exact-matches
  - /github/searching-for-information-on-github/searching-code
  - /github/searching-for-information-on-github/searching-on-github/searching-code
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - GitHub search
---

{% data reusables.search.you-can-search-globally %} For more information, see "[About searching on GitHub](/search-github/getting-started-with-searching-on-github/about-searching-on-github)."

Du kannst Code nur mit den diesen Qualifizierern der Codesuche durchsuchen. Spezifische Qualifizierer für Repositorys, Benutzer oder Commits funktionieren bei der Durchsuchung von Code nicht.

{% data reusables.search.syntax_tips %}

## Grundlegendes zur Codesuche

Aufgrund der Komplexität der Codesuche gelten bei der Durchführung der Suche Einschränkungen:

{% ifversion fpt or ghes or ghec %}
- {% data reusables.search.required_login %}{% endif %}
- Code in [Forks](/articles/about-forks) ist nur durchsuchbar, wenn für den Fork mehr Sterne vergeben wurden als für das übergeordnete Repository. Forks mit weniger Sternen als das übergeordnete Repository sind **nicht** für die Codesuche indiziert. Um Forks mit mehr Sternen als das übergeordnete Repository in die Suchergebnisse einzuschließen, musst Du Deiner Abfrage `fork:true` oder `fork:only` hinzufügen. Weitere Informationen findest Du unter „[Forks durchsuchen](/search-github/searching-on-github/searching-in-forks).“
- Only the _default branch_ is indexed for code search.{% ifversion fpt or ghec %}
- Nur Dateien kleiner 384 KB sind durchsuchbar.{% else %}* Nur Dateien kleiner 5 MB sind durchsuchbar.
- Nur die ersten 500 KB jeder Datei sind durchsuchbar.{% endif %}
- Only repositories with fewer than 500,000 files are searchable.{% ifversion fpt or ghec %}
- Only repositories that have had activity or have been returned in search results in the last year are searchable.{% endif %}
- Deine Quellcode-Suche muss mindestens einen Suchbegriff enthalten, ausgenommen bei [`filename`-Suchen](#search-by-filename). Beispielsweise ist eine Suche nach [`language:javascript`](https://github.com/search?utf8=%E2%9C%93&q=language%3Ajavascript&type=Code&ref=searchresults) ungültig, [`amazing language:javascript`](https://github.com/search?utf8=%E2%9C%93&q=amazing+language%3Ajavascript&type=Code&ref=searchresults) ist dagegen gültig.
- Die Suchergebnisse können maximal zwei gefundene Fragmente der gleichen Datei anzeigen, selbst wenn die Datei mehr Treffer enthält.
- Folgende Platzhalterzeichen können in Suchabfragen nicht verwendet werden: <code>. , : ; / \ ` ' " = * ! ? # $ & + ^ | ~ < > ( ) { } [ ] @</code>. Diese Zeichen werden bei der Suche schlicht ignoriert.

## Suche nach Dateiinhalten oder Dateipfad

Mit dem Qualifizierer `in` kannst Du Deine Suche auf den Inhalt der Quellcodedatei, auf den Dateipfad oder auf beides eingrenzen. Ohne diesen Qualifizierer werden nur Dateiinhalte durchsucht.

| Qualifizierer | Beispiel                                                                                                                                                     |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `in:file`     | [**octocat in:file**](https://github.com/search?q=octocat+in%3Afile&type=Code) durchsucht den Dateiinhalt nach dem Code „octocat“.                           |
| `in:path`     | [**octocat in:path**](https://github.com/search?q=octocat+in%3Apath&type=Code) durchsucht den Dateipfad nach dem Code „octocat“.                             |
|               | [**octocat in:file,path**](https://github.com/search?q=octocat+in%3Afile%2Cpath&type=Code) durchsucht Dateiinhalt und den Dateipfad nach dem Code „octocat“. |

## Suche innerhalb der Repositorys eines Benutzers oder einer Organisation

Wenn Sie Code in allen Repositorys suchen, die einem bestimmten Benutzer oder einer bestimmten Organisation gehören, verwenden Sie den Kennzeichner `user` bzw. `org`. Für die Suche nach Code in einem bestimmten Repository verwenden Sie den Kennzeichner `repo`.

| Qualifizierer             | Beispiel                                                                                                                                                                                                                               |
| ------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <code>user:<em>USERNAME</em></code> | [**user:defunkt extension:rb**](https://github.com/search?q=user%3Agithub+extension%3Arb&type=Code) sucht nach Code von @defunkt in Dateien mit der Erweiterung <em>.rb</em>.                                              |
| <code>org:<em>ORGNAME</em></code> | [**org:github extension:js**](https://github.com/search?utf8=%E2%9C%93&q=org%3Agithub+extension%3Ajs&type=Code) sucht nach Code von GitHub in Dateien mit der Erweiterung <em>.js</em>.                                    |
| <code>repo:<em>USERNAME/REPOSITORY</em></code> | [**repo:mozilla/shumway extension:as**](https://github.com/search?q=repo%3Amozilla%2Fshumway+extension%3Aas&type=Code) sucht nach Code aus dem Projekt „shumway“ von @mozilla in Dateien mit der Erweiterung <em>.as</em>. |

## Suche nach Standort

Mit dem Kennzeichner `path` können Sie nach Quellcode unter einem bestimmten Pfad innerhalb eines Repositorys suchen. Mit `path:/` suchen Sie nach Dateien auf der Root-Ebene eines Repositorys. Sie können aber auch einen Verzeichnisnamen oder den Pfad zu einem Verzeichnis angeben, um Dateien innerhalb dieses Verzeichnisses oder seiner Unterverzeichnisse zu durchsuchen.

| Qualifizierer              | Beispiel                                                                                                                                                                                                                                                                                                                         |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <code>path:/</code>  | [**octocat filename:readme path:/**](https://github.com/search?utf8=%E2%9C%93&q=octocat+filename%3Areadme+path%3A%2F&type=Code) sucht nach _readme_-Dateien mit dem Wort „octocat“ auf der Root-Ebene eines Repositorys.                                                                                                         |
| <code>path:<em>DIRECTORY</em></code>  | [**form path:cgi-bin language:perl**](https://github.com/search?q=form+path%3Acgi-bin+language%3Aperl&type=Code) matches Perl files with the word "form" in the <em>cgi-bin</em> directory, or in any of its subdirectories.                                                                                              |
| <code>path:<em>PATH/TO/DIRECTORY</em></code> | [**console path:app/public language:javascript**](https://github.com/search?q=console+path%3A%22app%2Fpublic%22+language%3Ajavascript&type=Code) matches JavaScript files with the word "console" in the <em>app/public</em> directory, or in any of its subdirectories (even if they reside in <em>app/public/js/form-validators</em>). |

## Suche nach Sprache
<!-- If you make changes to this feature, update /getting-started-with-github/github-language-support to reflect any changes. -->

Du kannst Code auch in Abhängigkeit der Programmiersprache suchen. The `language` qualifier can be the language name or alias. For a full list of supported languages with their names and aliases, see the [github/linguist repository](https://github.com/github/linguist/blob/master/lib/linguist/languages.yml).

| Qualifizierer              | Beispiel                                                                                                                                                                                                        |
| -------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <code>language:<em>LANGUAGE</em></code> | [**element language:xml size:100**](https://github.com/search?q=element+language%3Axml+size%3A100&type=Code) sucht Code mit dem Wort „element“, der als XML gekennzeichnet ist und genau 100 Byte groß ist.     |
|                            | [**display language:scss**](https://github.com/search?q=display+language%3Ascss&type=Code) sucht Code mit dem Wort „display“, der als SCSS gekennzeichnet ist.                                                  |
|                            | [**org:mozilla language:markdown**](https://github.com/search?utf8=%E2%9C%93&q=org%3Amozilla+language%3Amarkdown&type=Code) sucht Code aus allen Repositorys von @mozilla, der als Markdown gekennzeichnet ist. |

## Suche nach Dateigröße

Mit dem Kennzeichner `size` können Sie Quellcode auf Basis der Größe der Datei suchen, in der sich der Code befindet. `size` in Verbindung mit den [„Größer als“-, „Kleiner als“- und „Bereichs“-](/search-github/getting-started-with-searching-on-github/understanding-the-search-syntax)Operatoren filtert die Ergebnisse der Codesuche nach der Byte-Größe der Datei, die den Code enthält.

| Qualifizierer              | Beispiel                                                                                                                                                                                                                       |
| -------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| <code>size:<em>n</em></code> | [**function size:&gt;10000 language:python**](https://github.com/search?q=function+size%3A%3E10000+language%3Apython&type=Code) sucht Python-Code mit dem Wort „function“ in Dateien mit einer Größe von mehr als 10 KB. |

## Suche nach Dateiname

Der Kennzeichner `filename` sucht Codedateien mit einem bestimmten Dateinamen. Zur Suche nach Dateien in einem Repository können Sie aber auch die Dateisuche verwenden. Weitere Informationen findest Du unter „[Dateien auf GitHub suchen](/search-github/searching-on-github/finding-files-on-github).“

| Qualifizierer              | Beispiel                                                                                                                                                                                                                         |
| -------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <code>filename:<em>FILENAME</em></code> | [**filename:linguist**](https://github.com/search?utf8=%E2%9C%93&q=filename%3Alinguist&type=Code) sucht nach Dateien mit dem Dateinamen „linguist“.                                                                              |
|                            | [**filename:.vimrc commands**](https://github.com/search?q=filename%3A.vimrc+commands&type=Code) sucht *.vimrc*-Dateien, deren Namen das Wort „commands“ enthalten.                                                              |
|                            | [**filename:test_helper path:test language:ruby**](https://github.com/search?q=minitest+filename%3Atest_helper+path%3Atest+language%3Aruby&type=Code) sucht Ruby-Dateien mit dem Dateinamen *test_helper* im Verzeichnis *test*. |

## Suche nach Dateierweiterung

Der Kennzeichner `extension` sucht Codedateien mit einer bestimmten Dateierweiterung.

| Qualifizierer              | Beispiel                                                                                                                                                                                                                                             |
| -------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <code>extension:<em>EXTENSION</em></code> | [**form path:cgi-bin extension:pm**](https://github.com/search?q=form+path%3Acgi-bin+extension%3Apm&type=Code) sucht Code mit dem Wort „form“ in Dateien mit der Dateierweiterung <em>.pm</em> unter dem Pfad <em>cgi-bin</em>. |
|                            | [**icon size:>200000 extension:css**](https://github.com/search?utf8=%E2%9C%93&q=icon+size%3A%3E200000+extension%3Acss&type=Code) sucht Dateien größer als 200 KB mit der Dateierweiterung <em>.css</em> und dem Wort „icon" im Code.     |

## Weiterführende Informationen

- „[Suchergebnisse sortieren](/search-github/getting-started-with-searching-on-github/sorting-search-results/)“
- „[Durchsuchen von Forks](/search-github/searching-on-github/searching-in-forks)"{% ifversion fpt or ghec %}
- „[Navigieren von Code auf {% data variables.product.prodname_dotcom %}](/github/managing-files-in-a-repository/navigating-code-on-github)"{% endif %}
