---
title: Filtering and searching issues and pull requests
intro: 'To find detailed information about a repository on {% data variables.product.product_name %}, you can filter, sort, and search issues and pull requests that are relevant to the repository.'
redirect_from:
  - /github/managing-your-work-on-github/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-assignees
  - /articles/filtering-issues-and-pull-requests-by-assignees
  - /github/managing-your-work-on-github/filtering-issues-and-pull-requests-by-assignees
  - /github/managing-your-work-on-github/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-labels
  - /articles/filtering-issues-and-pull-requests-by-labels
  - /github/managing-your-work-on-github/filtering-issues-and-pull-requests-by-labels
  - /github/managing-your-work-on-github/finding-information-in-a-repository/filtering-issues-and-pull-requests
  - /articles/filtering-issues-and-pull-requests
  - /github/managing-your-work-on-github/filtering-issues-and-pull-requests
  - /github/managing-your-work-on-github/finding-information-in-a-repository/filtering-pull-requests-by-review-status
  - /articles/filtering-pull-requests-by-review-status
  - /github/managing-your-work-on-github/filtering-pull-requests-by-review-status
  - /github/managing-your-work-on-github/finding-information-in-a-repository
  - /articles/finding-information-in-a-repository
  - /github/managing-your-work-on-github/finding-information-in-a-repository/sharing-filters
  - /articles/sharing-filters
  - /github/managing-your-work-on-github/sharing-filters
  - /github/managing-your-work-on-github/finding-information-in-a-repository/using-search-to-filter-issues-and-pull-requests
  - /articles/using-search-to-filter-issues-and-pull-requests
  - /github/managing-your-work-on-github/using-search-to-filter-issues-and-pull-requests
  - /github/managing-your-work-on-github/finding-information-in-a-repository/sorting-issues-and-pull-requests
  - /articles/sorting-issues-and-pull-requests
  - /github/managing-your-work-on-github/sorting-issues-and-pull-requests
  - /github/administering-a-repository/finding-information-in-a-repository
  - /github/administering-a-repository/finding-information-in-a-repository/filtering-issues-and-pull-requests
  - /github/administering-a-repository/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-assignees
  - /github/administering-a-repository/finding-information-in-a-repository/filtering-issues-and-pull-requests-by-labels
  - /github/administering-a-repository/finding-information-in-a-repository/filtering-pull-requests-by-review-status
  - /github/administering-a-repository/finding-information-in-a-repository/sorting-issues-and-pull-requests
  - /github/administering-a-repository/finding-information-in-a-repository/using-search-to-filter-issues-and-pull-requests
  - /github/administering-a-repository/finding-information-in-a-repository/sharing-filters
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Issues
  - Pull requests
shortTitle: Filter and search
type: how_to
---

{% data reusables.cli.filter-issues-and-pull-requests-tip %}

## Issues und Pull Requests filtern

Issues und Pull Requests umfassen standardm????ige Filter, mit denen Du Deine Listen organisieren kannst.

{% data reusables.search.requested_reviews_search %}

Du kannst Issues und Pull Requests filtern, um Folgendes zu finden:
- alle offenen Issues und Pull Requests
- Issues und Pull Requests, die Du erstellt hast
- Issues und Pull Requests, die Dir zugewiesen sind
- Issues und Pull Requests, in denen Du [**@erw??hnt**](/articles/basic-writing-and-formatting-syntax/#mentioning-people-and-teams) wurdest

{% data reusables.cli.filter-issues-and-pull-requests-tip %}

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-issue-pr %}
3. Klicke auf **Filters** (Filter), um den gew??nschten Filtertyp auszuw??hlen. ![Dropdownmen?? zum Anwenden der Filter](/assets/images/help/issues/issues_filter_dropdown.png)

## Issues und Pull Requests nach Bearbeitern filtern

Once you've [assigned an issue or pull request to someone](/articles/assigning-issues-and-pull-requests-to-other-github-users), you can find items based on who's working on them.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-issue-pr %}
3. W??hle in der oberen rechten Ecke das Dropdownmen?? ???Assignee??? (Bearbeiter) aus.
4. In diesem Dropdownmen?? sind alle Benutzer aufgef??hrt, die Schreibzugriff auf Dein Repository haben. Klicke auf den Namen des Benutzers, dessen zugewiesene Elemente Du ansehen m??chtest, oder klicke auf **Assigned to nobody** (Niemandem zugewiesen), um zu sehen, welche Issues niemandem zugewiesen wurden. ![Dropdownmen?? ???Assignees??? (Bearbeiter) verwenden](/assets/images/help/issues/issues_assignee_dropdown.png)

{% tip %}

Um Deine Filterauswahl zur??ckzusetzen, klicke auf **Clear current search query, filters, and sorts** (Aktuelle Suchabfrage, Filter und Sortierung l??schen).

{% endtip %}

## Issues und Pull Requests nach Kennzeichnungen filtern

Once you've [applied labels to an issue or pull request](/articles/applying-labels-to-issues-and-pull-requests), you can find items based on their labels.

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-issue-pr %}
{% data reusables.project-management.labels %}
4. Klicke in der Liste der Kennzeichnungen auf eine Kennzeichnung, um die Issues und Pull Requests zu sehen, auf die sie angewendet wurde. ![Liste der Kennzeichnungen eines Repositorys](/assets/images/help/issues/labels-page.png)

{% tip %}

**Tipp:** Um Deine Filterauswahl zu l??schen, klicke auf **Clear current search query, filters, and sorts** (Aktuelle Suchabfrage, Filter und Sortierung l??schen).

{% endtip %}

## Pull Requests nach Review-Status filtern

Mit Filtern kannst Du Pull Requests nach Review-Status auflisten und Pull Requests suchen, die Du ??berpr??ft hast oder um deren Review Du von anderen gebeten wurdest.

Du kannst die Pull-Request-Liste eines Repositorys filtern, um folgende Pull Requests zu finden:
- Pull Requests, deren [Review](/articles/about-pull-request-reviews) noch aussteht
- Pull Requests, f??r die vor dem Merge [ein Review erforderlich ist](/github/administering-a-repository/about-protected-branches#require-pull-request-reviews-before-merging)
- Pull Requests, die ein Reviewer genehmigt hat
- Pull Requests, bei denen ein Reviewer um ??nderungen gebeten hat
- Pull requests that you have reviewed{% ifversion fpt or ghae or ghes > 3.2 or ghec %}
- Pull requests that someone has asked you directly to review{% endif %}
- Pull Requests, um denen [Du oder ein Team, bei dem Du Mitglied bist, um einen Review gebeten wurde](/articles/requesting-a-pull-request-review)

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-pr %}
3. W??hle in der oberen rechten Ecke das Dropdownmen?? ???Reviews??? (Reviews) aus. ![Dropdownmen?? ???Reviews??? (Reviews) im Filtermen?? ??ber der Liste der Pull Requests](/assets/images/help/pull_requests/reviews-filter-dropdown.png)
4. W??hle einen Filter aus, um alle Pull Requests mit dem Status dieses Filters zu finden. ![Liste der Filter im Dropdownmen?? ???Reviews??? (Reviews)](/assets/images/help/pull_requests/pr-review-filters.png)

## Issues und Pull Requests mit der Suchfunktion filtern

You can use advanced filters to search for issues and pull requests that meet specific criteria.

### Searching for issues and pull requests

{% include tool-switcher %}

{% webui %}

Mit der Suchleiste f??r Issues und Pull Requests kannst Du Deine eigenen benutzerdefinierten Filter erstellen und nach einer Vielzahl an Kriterien Sortierungen vornehmen. Die Suchleiste befindet sich auf den Registerkarten **Issues** und **Pull requests** jedes Repositorys und in Deinem [Dashboards f??r Issues und Pull Requests](/articles/viewing-all-of-your-issues-and-pull-requests).

![Die Suchleiste f??r Issues und Pull Requests](/assets/images/help/issues/issues_search_bar.png)

{% tip %}

**Tipp:** {% data reusables.search.search_issues_and_pull_requests_shortcut %}

{% endtip %}

{% endwebui %}

{% cli %}

{% data reusables.cli.cli-learn-more %}

You can use the {% data variables.product.prodname_cli %} to search for issues or pull requests. Use the `gh issue list` or `gh pr list` subcommand along with the `--search` argument and a search query.

For example, you can list, in order of date created, all issues that have no assignee and that have the label `help wanted` or `bug`.

```shell
gh issue list --search 'no:assignee label:"help wanted",bug sort:created-asc'
```

You can also list all pull requests that mention the `octo-org/octo-team` team.

```shell
gh pr list --search "team:octo-org/octo-team"
```

{% endcli %}

### About search terms

Mithilfe von Suchbegriffen zu Issues und Pull Requests kannst Du:

- Issues und Pull Requests nach Autor filtern: `state:open type:issue author:octocat`,
- Issues und Pull Requests filtern, die bestimmte Personen umfassen, sie jedoch nicht zwangsl??ufig [**@erw??hnen**](/articles/basic-writing-and-formatting-syntax/#mentioning-people-and-teams): `state:open type:issue involves:octocat`,
- Issues und Pull Requests nach Bearbeiter filtern: `state:open type:issue assignee:octocat`,
- Issues und Pull Requests nach Kennzeichnung filtern: `state:open type:issue label:"bug"`.
- Filter out search terms by using `-` before the term: `state:open type:issue -author:octocat`

{% ifversion fpt or ghes > 3.2 or ghae-next or ghec %}
{% tip %}

**Tip:** You can filter issues and pull requests by label using logical OR or using logical AND.
- To filter issues using logical OR, use the comma syntax: `label:"bug","wip"`.
- To filter issues using logical AND, use separate label filters: `label:"bug" label:"wip"`.

{% endtip %}
{% endif %}

{% ifversion fpt or ghes or ghae or ghec %}
F??r Issues kannst Du die Suche auf f??r folgendes benutzen:

- Filtere f??r Issues, die zu einem Pull Request ??ber eine schlie??ende Referenz verkn??pft sind:`linked:pr`
{% endif %}

Bei Pull Requests kannst Du die Suche auch verwenden, um:
- Pull Requests mit dem Status [Entwurf](/articles/about-pull-requests#draft-pull-requests) zu filtern: `is:draft`
- Pull Requests zu filtern, die noch keinem [Review](/articles/about-pull-request-reviews) unterzogen wurden: `state:open type:pr review:none`
- Pull Requests zu filtern, f??r die ein [Review erforderlich ist](/github/administering-a-repository/about-protected-branches#require-pull-request-reviews-before-merging), bevor sie gemergt werden k??nnen: `state:open type:pr review:required`,
- Von einem Reviewer genehmigte Pull Requests zu filtern: `state:open type:pr review:approved`
- Pull Requests zu filtern, in denen ein Reviewer um ??nderungen gebeten hat: `state:open type:pr review:changes_requested`
- Pull Requests nach [Reviewer](/articles/about-pull-request-reviews/) zu filtern: `state:open type:pr reviewed-by:octocat`
- Filter pull requests by the specific user [requested for review](/articles/requesting-a-pull-request-review): `state:open type:pr review-requested:octocat`{% ifversion fpt or ghae or ghes > 3.2 or ghec %}
- Filter pull requests that someone has asked you directly to review: `state:open type:pr user-review-requested:@me`{% endif %}
- Pull Requests nach einem Team filtern, das f??r dein Review angefordert wurde: `state:open type:pr team-review-requested:github/atom`{% ifversion fpt or ghes or ghae or ghec %}
- Nach Pull Requests filtern, die zu einem Issue verkn??pft sind, die der Pull Request schlie??en k??nnte: `linked:issue`{% endif %}

## Issues und Pull Requests sortieren

Zur besseren Darstellung der Informationen eines bestimmten Zeitraums k??nnen gefilterter Ansichten sortiert werden.

Du kannst jede gefilterte Ansicht nach folgenden Aspekten sortieren:

* Die neuesten Issues oder Pull Requests (nach Erstellungsdatum)
* Die ??ltesten Issues oder Pull Requests (nach Erstellungsdatum)
* Die Issues oder Pull Requests mit den meisten Kommentaren
* Die Issues oder Pull Requests mit den wenigsten Kommentaren
* Die neuesten Issues oder Pull Requests (nach ??nderungsdatum)
* Die ??ltesten Issues oder Pull Requests (nach ??nderungsdatum)
* The most added reaction on issues or pull requests

{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-issue-pr %}
1. W??hle oben rechts im Dropdownmen?? ???Sort??? (Sortieren) eine Option aus. ![Verwenden des Dropdownmen??s ???Sort??? (Sortieren)](/assets/images/help/issues/issues_sort_dropdown.png)

Zum Aufheben der Sortierung klicke auf **Sort** > **Newest** (Sortieren > Neueste).


## Filter freigeben

Wenn Du Issues und Pull Requests filterst oder sortierst, wird die URL Deines Browsers automatisch an die neue Ansicht angepasst.

Die hierbei generierte URL kannst Du anderen Benutzern senden, damit diese die gleiche Filteransicht aufrufen k??nnen.

W??rdest Du beispielsweise nach Issues filtern, die Hubot zugeordnet sind, und nach den ??ltesten offenen Issues sortieren, w??rde Deine URL in etwa wie folgt aussehen:

```
/issues?q=state:open+type:issue+assignee:hubot+sort:created-asc
```

## Weiterf??hrende Informationen

- "[Searching issues and pull requests](/articles/searching-issues)""
