---
title: Grundlegende Schreib- und Formatierungssyntax
intro: Erstelle mit einer einfachen Syntax eine ausgereifte Formatierung für Deine Texte und Codes auf GitHub.
redirect_from:
  - /articles/basic-writing-and-formatting-syntax
  - /github/writing-on-github/basic-writing-and-formatting-syntax
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
shortTitle: Basic formatting syntax
---

## Überschriften

Um eine Überschrift zu erstellen, füge bis zu sechs Rautenzeichen (`#`) vor dem Text der Überschrift hinzu. Die Anzahl an `#` bestimmt die Größe der Überschrift.

```markdown
# Die größte Überschrift
## Die zweitgrößte Überschrift
###### Die kleinste Überschrift
```

![Gerenderte H1-, H2- und H6-Überschriften](/assets/images/help/writing/headings-rendered.png)

## Textstil

You can indicate emphasis with bold, italic, or strikethrough text in comment fields and `.md` files.

| Stil                          | Syntax               | Tastenkürzel          | Beispiel                                 | Ausgabe                                |
| ----------------------------- | -------------------- | --------------------- | ---------------------------------------- | -------------------------------------- |
| Fett                          | `** **` oder `__ __` | Befehlstaste/Strg + B | `**Dieser Text ist fett.**`              | **Dieser Text ist fett.**              |
| Kursiv                        | `* *` oder `_ _`     | Befehlstaste/Strg + I | `*Dieser Text ist kursiv.*`              | *Dieser Text ist kursiv.*              |
| Durchgestrichen               | `~~ ~~`              |                       | `~~Dieser Text war falsch.~~`            | ~~Dieser Text war falsch.~~            |
| Fett und kursiv verschachtelt | `** **` und `_ _`    |                       | `**Dieser Text ist _sehr_ wichtig.**`    | **Dieser Text ist _sehr_ wichtig.**    |
| Alles fett und kursiv         | `*** ***`            |                       | `***Dieser gesamte Text ist wichtig.***` | ***Dieser gesamte Text ist wichtig.*** |

## Text zitieren

Du kannst einen Text mit einem `>` zitieren.

```markdown
Text that is not a quote

> Text that is a quote
```

![Gerenderter zitierter Text](/assets/images/help/writing/quoted-text-rendered.png)

{% tip %}

**Tipp:** Beim Anzeigen einer Unterhaltung kannst Du Text in einem Kommentar automatisch zitieren, indem Du den Text markierst und dann `r` eingibst. Du kannst einen vollständigen Kommentar zitieren, indem Du auf {% octicon "kebab-horizontal" aria-label="The horizontal kebab icon" %} und dann auf **Quote reply** (Antwort mit Zitat) klickst. Weitere Informationen zu Tastenkürzeln findest Du unter „[Tastenkürzel](/articles/keyboard-shortcuts/).“

{% endtip %}

## Code zitieren

Du kannst Code oder einen Befehl innerhalb eines Satzes mit einfachen Backticks zitieren. The text within the backticks will not be formatted.{% ifversion fpt or ghae-next or ghes > 3.1 or ghec %} You can also press the `command` or `Ctrl` + `e` keyboard shortcut to insert the backticks for a code block within a line of Markdown.{% endif %}

```markdown
Verwende `git status`, um alle neuen oder geänderten Dateien aufzulisten, die noch nicht freigegeben wurden.
```

![Gerenderter Inline-Codeblock](/assets/images/help/writing/inline-code-rendered.png)

Um Code oder einen Text in einem eigenen Absatz zu formatieren, verwende dreifache Backticks.

<pre>
Zu den grundlegenden Git-Befehlen gehören:
```
git status
git add
git commit
```
</pre>

![Gerenderter Codeblock](/assets/images/help/writing/code-block-rendered.png)

Weitere Informationen findest Du unter „[Erstellen und Hervorheben von Codeblöcken](/articles/creating-and-highlighting-code-blocks).“

## Links

Du kannst einen Inline-Link erstellen, indem Du den Text in eckige Klammern `[ ]` einschließt und dann die URL in runde Klammern `( )` einschließt. {% ifversion fpt or ghae-next or ghes > 3.1 or ghec %}You can also use the keyboard shortcut `command + k` to create a link.{% endif %}

`Diese Website wurde mit [GitHub Pages](https://pages.github.com/) erstellt.`

![Gerenderter Link](/assets/images/help/writing/link-rendered.png)

{% tip %}

**Tipp:** {% data variables.product.product_name %} erstellt automatisch Links, wenn Du gültige URLs in einen Kommentar einfügst. Weitere Informationen findest Du unter „[Automatisch verknüpfte Verweise und URLs](/articles/autolinked-references-and-urls).“

{% endtip %}

## Links zu Abschnitten

{% data reusables.repositories.section-links %}

## Relative Links

{% data reusables.repositories.relative-links %}

## Images

You can display an image by adding `!` and wrapping the alt text in`[ ]`. Then wrap the link for the image in parentheses `()`.

`![This is an image](https://myoctocat.com/assets/images/base-octocat.svg)`

![Rendered Image](/assets/images/help/writing/image-rendered.png)

{% data variables.product.product_name %} supports embedding images into your issues, pull requests{% ifversion fpt or ghec %}, discussions{% endif %}, comments  and `.md` files. You can display an image from your repository, add a link to an online image, or upload an image. For more information, see "[Uploading assets](#uploading-assets)."

{% tip %}

**Tip:** When you want to display an image which is in your repository, you should use relative links instead of absolute links.

{% endtip %}

Here are some examples for using relative links to display an image.

| Context                                                     | Relative Link                                                          |
| ----------------------------------------------------------- | ---------------------------------------------------------------------- |
| In a `.md` file on the same branch                          | `/assets/images/electrocat.png`                                        |
| In a `.md` file on another branch                           | `/../main/assets/images/electrocat.png`                                |
| In issues, pull requests and comments of the repository     | `../blob/main/assets/images/electrocat.png`                            |
| In a `.md` file in another repository                       | `/../../../../github/docs/blob/main/assets/images/electrocat.png`      |
| In issues, pull requests and comments of another repository | `../../../github/docs/blob/main/assets/images/electrocat.png?raw=true` |

{% note %}

**Note**: The last two relative links in the table above will work for images in a private repository only if the viewer has at least read access to the private repository which contains these images.

{% endnote %}

For more information, see "[Relative Links](#relative-links)."


## Listen

Du kannst eine ungeordnete Liste erstellen, indem Du einer Textzeile oder mehreren Textzeilen ein `-` oder `*` voranstellst.

```markdown
- George Washington
- John Adams
- Thomas Jefferson
```

![Gerenderte ungeordnete Liste](/assets/images/help/writing/unordered-list-rendered.png)

Um Deine Liste zu ordnen, stelle jeder Zeile eine Zahl voran.

```markdown
1. James Madison
2. James Monroe
3. John Quincy Adams
```

![Gerenderte geordnete Liste](/assets/images/help/writing/ordered-list-rendered.png)

### Verschachtelte Listen

Du kannst eine verschachtelte Liste erstellen, indem Du ein Listenelement oder mehrere Listenelemente unter einem anderen Element einrückst.

Beim Web-Editor auf {% data variables.product.product_name %} oder bei einem Texteditor wie [Atom](https://atom.io/), der eine nicht proportionale Schriftart verwendet, kannst Du Deine Liste visuell ausrichten. Gib vor dem einzurückenden Listenelement so viele Leerzeichen ein, bis das Listenzeichen (`-` oder `*`) direkt unter dem ersten Zeichen des darüber liegenden Elements liegt.

```markdown
1. First list item
   - First nested list item
     - Second nested list item
```

![Verschachtelte Liste mit hervorgehobener Ausrichtung](/assets/images/help/writing/nested-list-alignment.png)

![Liste mit zwei Ebenen untergeordneter Elemente](/assets/images/help/writing/nested-list-example-1.png)

Um eine verschachtelte Liste im Kommentareditor auf {% data variables.product.product_name %} zu erstellen, der keine nicht proportionale Schriftart verwendet, kannst Du Dir das Listenelement direkt über der verschachtelten Liste ansehen und die Anzahl der Zeichen zählen, die vor dem Inhalt dieses Elements stehen. Gib diese Anzahl an Leerzeichen dann vor dem untergeordneten Listenelement ein.

Im folgenden Beispiel kannst Du ein untergeordnetes Listenelement unter dem Listenelement `100. <code>Erstes Listenelement` hinzufügen, indem Du das untergeordnete Listenelement um mindestens fünf Leerzeichen einrückst, da sich vor `Erstes Listenelement` fünf Zeichen (`100.`) befinden.

```markdown
100. Erstes Listenelement
     - Erstes untergeordnetes Listenelement
```

![Liste mit einem untergeordneten Listenelement](/assets/images/help/writing/nested-list-example-3.png)

Du kannst mit derselben Methode mehrere Ebenen an verschachtelten Listen erstellen. For example, because the first nested list item has seven characters (`␣␣␣␣␣-␣`) before the nested list content `First nested list item`, you would need to indent the second nested list item by seven spaces.

```markdown
100. Erstes Listenelement
     - Erstes untergeordnetes Listenelement
       - Zweites untergeordnetes Listenelement
```

![Liste mit zwei Ebenen untergeordneter Elemente](/assets/images/help/writing/nested-list-example-2.png)

Weitere Beispiele findest Du in den [GitHub Flavored Markdown-Spezifikationen](https://github.github.com/gfm/#example-265).

## Aufgabenlisten

{% data reusables.repositories.task-list-markdown %}

Wenn die Beschreibung eines Aufgabenlistenelements mit einer Klammer beginnt, müssen Sie die Klammer mit einem `\` maskieren:

`- [ ] \(Optional) Öffne einen Issue zur Nachverfolgung`

Weitere Informationen findest Du unter „[Informationen zu Aufgabenlisten](/articles/about-task-lists).“

## Personen und Teams erwähnen

Du kannst auf {% data variables.product.product_name %} eine Person oder ein [Team](/articles/setting-up-teams/) erwähnen, indem Du `@` gefolgt vom Benutzer- respektive Teamnamen eingibst. This will trigger a notification and bring their attention to the conversation. Wenn Du einen Kommentar bearbeitest und dabei den Benutzer- oder Teamnamen erwähnst, wird die Person respektive das Team ebenfalls benachrichtigt. Weitere Informationen zu Benachrichtigungen findest Du unter {% ifversion fpt or ghes or ghae or ghec %}„[Über Benachrichtigungen](/github/managing-subscriptions-and-notifications-on-github/about-notifications){% else %}„[Über Benachrichtigungen](/github/receiving-notifications-about-activity-on-github/about-notifications){% endif %}."

`@github/support Wie findet ihr diese Aktualisierungen?`

![Gerenderte @Erwähnung](/assets/images/help/writing/mention-rendered.png)

Wenn Du ein übergeordnetes Team erwähnst, erhalten auch die Mitglieder untergeordneter Teams Benachrichtigungen, was die Kommunikation mit mehreren Personengruppen erleichtert. Weitere Informationen finden Sie unter „[Informationen zu Teams](/articles/about-teams)“.

Wenn Du das Zeichen `@` eingibst, wird eine Liste der Personen oder Teams eines Projektes angezeigt. Diese Liste wird während Deiner Eingabe gefiltert. Wenn Du den Namen der gewünschten Person respektive des gewünschten Teams siehst, kannst Du ihn mit den Pfeiltasten auswählen und die Tabulator- oder Eingabetaste drücken, um den Namen zu vervollständigen. Wenn Du Teams erwähnen möchtest, gib den @Organisations-/Teamnamen ein. Alle Mitglieder des Teams werden die Unterhaltung daraufhin abonniert erhalten.

Die automatisch vervollständigten Ergebnisse sind auf Repository-Mitarbeiter und andere Thread-Teilnehmer beschränkt.

## Auf Issues und Pull Requests verweisen

Du kannst eine Liste vorgeschlagener Issues und Pull Requests im Repository anzeigen, indem Du `#` eingibst. Gib die Nummer des Issues oder Pull Requests ein, um die Liste zu filtern, und drücke dann die Tabulator- oder Eingabetaste, um das markierte Ergebnis zu vervollständigen.

Weitere Informationen findest Du unter „[Automatisch verknüpfte Verweise und URLs](/articles/autolinked-references-and-urls).“

## Auf externe Ressourcen verweisen

{% data reusables.repositories.autolink-references %}

## Inhaltsanhänge

Some {% data variables.product.prodname_github_apps %} provide information in {% data variables.product.product_name %} for URLs that link to their registered domains. {% data variables.product.product_name %} zeigt die von der App bereitgestellten Informationen unter der URL im Text oder Kommentar eines Issues bzw. Pull Requests an.

![Inhaltsanhang](/assets/images/github-apps/content_reference_attachment.png)

Um Inhaltsanhänge zu sehen, musst Du eine {% data variables.product.prodname_github_app %} besitzen, die das API für Inhaltsanhänge nutzt, welche auf dem Repository installiert ist.{% ifversion fpt or ghec %} Weitere Informationen findest Du unter „[Eine App in Deinem persönlichen Konto installieren](/articles/installing-an-app-in-your-personal-account)“ und „[Eine App in Deiner Organisation installieren](/articles/installing-an-app-in-your-organization)“.{% endif %}

Für URLs, die Teil eines Markdown-Links sind, werden keine Inhaltsanhänge angezeigt.

For more information about building a {% data variables.product.prodname_github_app %} that uses content attachments, see "[Using Content Attachments](/apps/using-content-attachments)."

## Uploading assets

You can upload assets like images by dragging and dropping, selecting from a file browser, or pasting. You can upload assets to issues, pull requests, comments, and `.md` files in your repository.

## Emojis verwenden

Du kannst Emojis einfügen, indem Du `:EMOJICODE:` eingeben.

`@octocat :+1: Dieser Pull Request sieht gut aus. Er ist bereit zum Mergen! :shipit:`

![Gerendertes Emoji](/assets/images/help/writing/emoji-rendered.png)

Bei der Eingabe von `:` wird eine Liste mit Vorschlägen für Emojis angezeigt. Die Liste wird während der Eingabe gefiltert. Wenn Du den gewünschten Emoji siehst, drücke die **Tabulator-** oder **Eingabetaste**, um das markierte Ergebnis zu vervollständigen.

For a full list of available emoji and codes, check out [the Emoji-Cheat-Sheet](https://github.com/ikatyang/emoji-cheat-sheet/blob/master/README.md).

## Paragraphen

Um einen neuen Absatz zu erstellen, lasse eine Zeile zwischen den Textzeilen leer.

{% ifversion fpt or ghae-next or ghes > 3.3 or ghec %}
## Footnotes

You can add footnotes to your content by using this bracket syntax:

```
Here is a simple footnote[^1].

A footnote can also have multiple lines[^2].  

You can also use words, to fit your writing style more closely[^note].

[^1]: My reference.
[^2]: Every new line should be prefixed with 2 spaces.  
  This allows you to have a footnote with multiple lines.
[^note]:
    Named footnotes will still render with numbers instead of the text but allow easier identification and linking.  
    This footnote also has been made with a different syntax using 4 spaces for new lines.
```

The footnote will render like this:

![Rendered footnote](/assets/images/site/rendered-footnote.png)

{% tip %}

**Note**: The position of a footnote in your Markdown does not influence where the footnote will be rendered. You can write a footnote right after your reference to the footnote, and the footnote will still render at the bottom of the Markdown.

{% endtip %}
{% endif %}

## Hiding content with comments

You can tell {% data variables.product.product_name %} to hide content from the rendered Markdown by placing the content in an HTML comment.

<pre>
&lt;!-- This content will not appear in the rendered Markdown --&gt;
</pre>

## Markdown-Formatierung ignorieren

Sie können {% data variables.product.product_name %} anweisen, die Markdown-Formatierung zu ignorieren, indem Sie das Markdown-Zeichen mit `\` maskieren.

`Wir benennen \*unser-neues-Projekt\* in \*unser-altes-Projekt\* um.`

![Gerendertes maskiertes Zeichen](/assets/images/help/writing/escaped-character-rendered.png)

Weitere Informationen findest Du unter „[Markdown-Syntax](https://daringfireball.net/projects/markdown/syntax#backslash)“ von Daring Fireball.

{% ifversion fpt or ghes > 3.2 or ghae-issue-5232 or ghec %}

## Disabling Markdown rendering

{% data reusables.repositories.disabling-markdown-rendering %}

{% endif %}

## Weiterführende Informationen

- [{% data variables.product.prodname_dotcom %} Flavored Markdown – Spezifikation](https://github.github.com/gfm/)
- „[Informationen zum Schreiben und Formatieren bei GitHub](/articles/about-writing-and-formatting-on-github)“
- „[Mit erweiterter Formatierung arbeiten](/articles/working-with-advanced-formatting)“
- „[Markdown meistern](https://guides.github.com/features/mastering-markdown/)“
