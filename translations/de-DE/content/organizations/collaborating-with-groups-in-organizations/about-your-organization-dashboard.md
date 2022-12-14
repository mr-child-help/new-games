---
title: Informationen zum Dashboard Deiner Organisation
intro: 'Als Organisationsmitglied kannst Du jederzeit das Dashboard Deiner Organisation aufrufen, um über die neuesten Aktivitäten auf dem Laufenden zu bleiben und Issues und Pull Requests zu beobachten, die Du in der Organisation bearbeitest oder verfolgst.'
redirect_from:
  - /articles/about-your-organization-dashboard
  - /github/setting-up-and-managing-organizations-and-teams/about-your-organization-dashboard
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Organizations
  - Teams
shortTitle: Organization dashboard
---

## Auf das Dashboard Deiner Organisation zugreifen

{% data reusables.dashboard.access-org-dashboard %}

## Neueste Aktivitäten finden

Im Abschnitt „Recent activity" (Neueste Aktivitäten) Deines Newsfeed kannst Du schnell die zuletzt aktualisierten Issues und Pull Requests in Deiner Organisation finden und weiterverfolgen.

{% data reusables.dashboard.recent-activity-qualifying-events %}

## Repositorys in Deiner Organisation finden

Über die linke Seitenleiste Deines Dashboards kannst Du auf die wichtigsten Repositorys Deines Unternehmens zugreifen, in denen Du aktiv bist.

![Liste der Repositorys, in denen Du in Deiner Organisation am aktivsten bist](/assets/images/help/dashboard/repositories-from-organization-dashboard.png)

## Über Aktivitäten in der Organisation auf dem Laufenden bleiben

Im Bereich "Alle Aktivitäten" Deines Newsfeed kannst Du Aktualisierungen von anderen Teams und Repositorys in Deiner Organisation ansehen.

Der Abschnitt "Alle Aktivitäten" zeigt alle aktuellen Aktivitäten in der Organisation, einschließlich Aktivitäten in Repositorys, die Du nicht abonniert hast, und von Personen, denen Du nicht folgst. For more information, see {% ifversion fpt or ghes or ghae or ghec %}"[About notifications](/github/managing-subscriptions-and-notifications-on-github/about-notifications){% else %}"[Watching and unwatching repositories](/github/receiving-notifications-about-activity-on-github/watching-and-unwatching-repositories){% endif %}" and "[Following people](/articles/following-people)."

Beispielsweise werden im Newsfeed der Organisation Aktualisierungen angezeigt, wenn jemand in der Organisation:
 - einen neuen Branch erstellt,
 - einen Issue oder Pull Request kommentiert,
 - einen Pull-Request-Review-Kommentar absendet,
 - ein Repository forkt,
 - eine Wiki-Seite erstellt,
 - Pushes commits.{% ifversion fpt or ghes or ghec %}
 - Creates a public repository.{% endif %}

## Weiterführende Informationen

- „[Informationen zum persönlichen Dashboard](/articles/about-your-personal-dashboard)“
