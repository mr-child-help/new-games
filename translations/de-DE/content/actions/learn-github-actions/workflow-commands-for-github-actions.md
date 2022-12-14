---
title: Workflow-Befehle für GitHub-Aktionen
shortTitle: Workflow-Befehle
intro: 'Du kannst Workflow-Befehle verwenden, wenn Du Shell-Befehle in einem Workflow oder im Code einer Aktion ausführst.'
redirect_from:
  - /articles/development-tools-for-github-actions
  - /github/automating-your-workflow-with-github-actions/development-tools-for-github-actions
  - /actions/automating-your-workflow-with-github-actions/development-tools-for-github-actions
  - /actions/reference/development-tools-for-github-actions
  - /actions/reference/logging-commands-for-github-actions
  - /actions/reference/workflow-commands-for-github-actions
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
---

{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

## Informationen zu Workflow-Befehlen

Aktionen können mit dem Runner-Rechner kommunizieren, um Umgebungsvariablen zu setzen, Werte zur Verwendung in anderen Aktionen auszugeben, Debug-Meldungen zu den Ausgabeprotokollen zuzufügen und für andere Zwecke.

Most workflow commands use the `echo` command in a specific format, while others are invoked by writing to a file. For more information, see ["Environment files".](#environment-files)

``` bash
echo "::workflow-command parameter1={data},parameter2={data}::{command value}"
```

{% note %}

**Hinweis:** Bei Workflow-Befehl und Parameternamen wird nicht zwischen Groß- und Kleinschreibung unterschieden.

{% endnote %}

{% warning %}

**Warnung:** Wenn Du die Kommandozeile verwendest, lass bei Workflow-Befehlen die doppelten Anführungszeichen (`"`) weg.

{% endwarning %}

## Workflow-Befehle verwenden, um auf Funktionen des Toolkits zuzugreifen

Das [actions/toolkit](https://github.com/actions/toolkit) enthält eine Reihe von Funktionen, die als Workflow-Befehle ausgeführt werden können. Verwende die Syntax `::`, um die Workflow-Befehle in Deiner YAML-Datei auszuführen. Diese Befehle werden dann über `stdout` an den Runner gesandt. For example, instead of using code to set an output, as below:

```javascript
core.setOutput('SELECTED_COLOR', 'green');
```

You can use the `set-output` command in your workflow to set the same value:

{% raw %}
``` yaml
      - name: Set selected color
        run: echo '::set-output name=SELECTED_COLOR::green'
        id: random-color-generator
      - name: Get color
        run: echo "The selected color is ${{ steps.random-color-generator.outputs.SELECTED_COLOR }}"
```
{% endraw %}

Die folgende Tabelle zeigt, welche Toolkit-Funktionen innerhalb eines Workflows verfügbar sind:

| Toolkit-Funktion      | Äquivalenter Workflow-Befehl                                          |
| --------------------- | --------------------------------------------------------------------- |
| `core.addPath`        | Accessible using environment file `GITHUB_PATH`                       |
| `core.debug`          | `debug` |{% ifversion fpt or ghes > 3.2 or ghae-issue-4929 or ghec %}
| `core.notice`         | `notice` 
{% endif %}
| `core.error`          | `error`                                                               |
| `core.endGroup`       | `endgroup`                                                            |
| `core.exportVariable` | Accessible using environment file `GITHUB_ENV`                        |
| `core.getInput`       | Zugänglich durch Umgebungsvariable `INPUT_{NAME}`                     |
| `core.getState`       | Zugänglich durch Umgebungsvariable `STATE_{NAME}`                     |
| `core.isDebug`        | Zugänglich durch Umgebungsvariable `RUNNER_DEBUG`                     |
| `core.saveState`      | `save-state`                                                          |
| `core.setFailed`      | Wird als Abkürzung für `::error` und `exit 1` verwendet               |
| `core.setOutput`      | `set-output`                                                          |
| `core.setSecret`      | `add-mask`                                                            |
| `core.startGroup`     | `Gruppe`                                                              |
| `core.warning`        | `warnung`                                                             |

## Setting an output parameter

```
::set-output name={name}::{value}
```

Legt den Ausgabeparameter einer Aktion fest.

Optional kannst Du auch Ausgabeparameter in der Metadaten-Datei einer Aktion deklarieren. Weitere Informationen findest Du unter „[Metadaten-Syntax für {% data variables.product.prodname_actions %}](/articles/metadata-syntax-for-github-actions#outputs)“.

### Beispiel

``` bash
echo "::set-output name=action_fruit::strawberry"
```

## Setting a debug message

```
::debug::{message}
```

Gibt eine Debugging-Meldung im Protokoll aus. Du musst ein Geheimnis mit dem Namen `ACTIONS_STEP_DEBUG` und dem Wert `true` erstellen, um die durch diesen Befehl gesetzten Debugging-Meldungen im Protokoll zu sehen. For more information, see "[Enabling debug logging](/actions/managing-workflow-runs/enabling-debug-logging)."

### Beispiel

``` bash
echo "::debug::Set the Octocat variable"
```

{% ifversion fpt or ghes > 3.2 or ghae-issue-4929 or ghec %}

## Setting a notice message

```
::notice file={name},line={line},endLine={endLine},title={title}::{message}
```

Creates a notice message and prints the message to the log. {% data reusables.actions.message-annotation-explanation %}

{% data reusables.actions.message-parameters %}

### Beispiel

``` bash
echo "::notice file=app.js,line=1,col=5,endColumn=7::Missing semicolon"
```

{% endif %}

## Setting a warning message

```
::warning file={name},line={line},endLine={endLine},title={title}::{message}
```

Erstellt eine Warnmeldung und fügt die Mitteilung in das Protokoll ein. {% data reusables.actions.message-annotation-explanation %}

{% data reusables.actions.message-parameters %}

### Beispiel

``` bash
echo "::warning file=app.js,line=1,col=5,endColumn=7::Missing semicolon"
```

## Setting an error message

```
::error file={name},line={line},endLine={endLine},title={title}::{message}
```

Erstellt eine Fehlermeldung und fügt die Mitteilung in das Protokoll ein. {% data reusables.actions.message-annotation-explanation %}

{% data reusables.actions.message-parameters %}

### Beispiel

``` bash
echo "::error file=app.js,line=1,col=5,endColumn=7::Missing semicolon"
```

## Grouping log lines

```
::group::{title}
::endgroup::
```

Creates an expandable group in the log. To create a group, use the `group` command and specify a `title`. Anything you print to the log between the `group` and `endgroup` commands is nested inside an expandable entry in the log.

### Beispiel

```bash
echo "::group::My title"
echo "Inside group"
echo "::endgroup::"
```

![Foldable group in workflow run log](/assets/images/actions-log-group.png)

## Masking a value in log

```
::add-mask::{value}
```

Das Maskieren eines Werts verhindert, dass ein String oder eine Variable im Protokoll ausgegeben werden. Jedes maskierte Wort, getrennt durch Leerzeichen, wird durch das Zeichen `*` ersetzt. Du kannst eine Umgebungsvariable oder einen String für den Wert (`value`) der Maske verwenden.

### Beispiel für das Maskieren eines Strings

Wenn Du `"Mona The Octocat"` im Protokoll ausgibst, siehst Du `"***"`.

```bash
echo "::add-mask::Mona The Octocat"
```

### Beispiel für das Maskieren einer Umgebungsvariablen

Wenn Du die Variable `MY_NAME` oder den Wert `"Mona The Octocat"` ins Protokoll ausgibst, siehst Du `"***"` statt `"Mona The Octocat"`.

```bash
MY_NAME="Mona The Octocat"
echo "::add-mask::$MY_NAME"
```

## Stopping and starting workflow commands

`::stop-commands::{endtoken}`

Stops processing any workflow commands. This special command allows you to log anything without accidentally running a workflow command. Du kannst beispielsweise die Protokollierung anhalten, um ein vollständiges Skript mit Kommentaren auszugeben.

To stop the processing of workflow commands, pass a unique token to `stop-commands`. To resume processing workflow commands, pass the same token that you used to stop workflow commands.

{% warning %}

**Warning:** Make sure the token you're using is randomly generated and unique for each run. As demonstrated in the example below, you can generate a unique hash of your `github.token` for each run.

{% endwarning %}

```
::{endtoken}::
```

### Example stopping and starting workflow commands

{% raw %}

```yaml
jobs:
  workflow-command-job:
    runs-on: ubuntu-latest
    steps:
      - name: disable workflow commands
        run: |
          echo '::warning:: this is a warning'
          echo "::stop-commands::`echo -n ${{ github.token }} | sha256sum | head -c 64`"
          echo '::warning:: this will NOT be a warning'
          echo "::`echo -n ${{ github.token }} | sha256sum | head -c 64`::"
          echo '::warning:: this is a warning again'
```

{% endraw %}

## Werte an die „Pre-“ (Vor-) und „Post-“ (Nach-)Aktionen senden

Mit dem Befehl `save-state` kannst Du Umgebungsvariablen für den Datenaustausch mit der `pre:`- oder `post:`-Aktionen Deines Workflows erzeugen. Zum Beispiel kannst Du mit der `pre:`-Aktion eine Datei erstellen, den Datei-Speicherort an die `main:`-Aktion übergeben und dann mit der `post:`-Aktion die Datei löschen. Alternativ kannst Du eine Datei mit der `main:`-Aktion erstellen, den Dateipfad an die `post:`-Aktion übergeben und ebenfalls mit der `post:`-Aktion die Datei löschen.

Wenn Du mehrere `pre:`- oder `post:`-Aktionen hast, kannst Du auf den gespeicherten Wert nur in der Aktion zugreifen, in der `save-state` verwendet wurde. Weitere Informationen zur `post:`-Aktion findest Du unter „[Metadaten-Syntax für {% data variables.product.prodname_actions %}](/actions/creating-actions/metadata-syntax-for-github-actions#post)“.

Der Befehl `save-state` kann nur innerhalb einer Aktion ausgeführt werden und ist für YAML Dateien nicht verfügbar. Der gespeicherte Wert wird als Umgebungswert mit dem Präfix `STATE_` gespeichert.

Dieses Beispiel verwendet JavaScript, um den Befehl `save-state` auszuführen. Die resultierende Umgebungsvariable heißt `STATE_processID` und hat den Wert `12345`:

``` javascript
console.log('::save-state name=processID::12345')
```

Die Variable `STATE_processID` ist dann exklusiv für das Bereinigungsskript verfügbar, das unter der `main`-Aktion ausgeführt wird. Dieses Beispiel läuft in `main` und verwendet JavaScript, um den Wert anzuzeigen, der der `STATE_processID` Umgebungsvariable zugewiesen wurde:

``` javascript
console.log("The running PID from the main action is: " +  process.env.STATE_processID);
```

## Environment Files

During the execution of a workflow, the runner generates temporary files that can be used to perform certain actions. The path to these files are exposed via environment variables. You will need to use UTF-8 encoding when writing to these files to ensure proper processing of the commands. Multiple commands can be written to the same file, separated by newlines.

{% warning %}

**Warning:** Powershell does not use UTF-8 by default. Make sure you write files using the correct encoding. For example, you need to set UTF-8 encoding when you set the path:

```yaml
steps:
  - run: echo "mypath" | Out-File -FilePath $env:GITHUB_PATH -Encoding utf8 -Append
```

{% endwarning %}

## Setting an environment variable

``` bash
echo "{name}={value}" >> $GITHUB_ENV
```

Creates or updates an environment variable for any steps running next in a job. The step that creates or updates the environment variable does not have access to the new value, but all subsequent steps in a job will have access. Bei Umgebungsvariablen wird die Groß- und Kleinschreibung berücksichtigt. Sie können auch Satzzeichen enthalten.

{% note %}

**Note:** Environment variables must be explicitly referenced using the [`env` context](/actions/reference/context-and-expression-syntax-for-github-actions#env-context) in expression syntax or through use of the `$GITHUB_ENV` file directly; environment variables are not implicitly available in shell commands.

{% endnote %}

### Beispiel

{% raw %}
```
steps:
  - name: Set the value
    id: step_one
    run: |
      echo "action_state=yellow" >> $GITHUB_ENV
  - name: Use the value
    id: step_two
    run: |
      echo "${{ env.action_state }}" # This will output 'yellow'
```
{% endraw %}

### Multiline strings

For multiline strings, you may use a delimiter with the following syntax.

```
{name}<<{delimiter}
{value}
{delimiter}
```

#### Beispiel

In this example, we use `EOF` as a delimiter and set the `JSON_RESPONSE` environment variable to the value of the curl response.
```yaml
steps:
  - name: Set the value
    id: step_one
    run: |
      echo 'JSON_RESPONSE<<EOF' >> $GITHUB_ENV
      curl https://httpbin.org/json >> $GITHUB_ENV
      echo 'EOF' >> $GITHUB_ENV
```

## Adding a system path

``` bash
echo "{path}" >> $GITHUB_PATH
```

Prepends a directory to the system `PATH` variable and automatically makes it available to all subsequent actions in the current job; the currently running action cannot access the updated path variable. To see the currently defined paths for your job, you can use `echo "$PATH"` in a step or an action.

### Beispiel

This example demonstrates how to add the user `$HOME/.local/bin` directory to `PATH`:

``` bash
echo "$HOME/.local/bin" >> $GITHUB_PATH
```
