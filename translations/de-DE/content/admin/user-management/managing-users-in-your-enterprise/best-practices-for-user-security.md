---
title: Best Practices für die Benutzersicherheit
intro: '{% ifversion ghes %}Outside of instance-level security measures (SSL, subdomain isolation, configuring a firewall) that a site administrator can implement, there {% else %}There {% endif %}are steps your users can take to help protect your enterprise.'
redirect_from:
  - /enterprise/admin/user-management/best-practices-for-user-security
  - /admin/user-management/best-practices-for-user-security
versions:
  ghes: '*'
  ghae: '*'
type: reference
topics:
  - Enterprise
  - Security
  - User account
shortTitle: User security best practices
---

{% ifversion ghes %}
## Zwei-Faktor-Authentifizierung aktivieren

Mittels Zwei-Faktor-Authentifizierung (2FA) können Sie sich bei Websites und Diensten anmelden, die zusätzlich zur Eingabe eines Passworts zur Authentifizierung einen zweiten Faktor vorschreiben. Im Falle von {% data variables.product.prodname_ghe_server %} ist dieser zweite Faktor ein einmaliger Authentifizierungscode, der von einer Anwendung auf dem Smartphone eines Benutzers generiert wird. Sie sollten unbedingt festlegen, dass Benutzer die Zwei-Faktor-Authentifizierung für ihre Konten aktivieren müssen. Mit der Zwei-Faktor-Authentifizierung müssten das Passwort des Benutzers und dessen Smartphone kompromittiert werden, damit das Konto an sich kompromittiert werden kann.

Weitere Informationen zum Konfigurieren der Zwei-Faktor-Authentifizierung finden Sie unter „[Informationen zur Zwei-Faktor-Authentifizierung](/enterprise/{{ currentVersion }}/user/articles/about-two-factor-authentication)“.
{% endif %}

## Passwort-Manager vorschreiben

We strongly recommend requiring your users to install and use a password manager--such as [LastPass](https://lastpass.com/) or [1Password](https://1password.com/)--on any computer they use to connect to your enterprise. Dadurch wird gewährleistet, dass Passwörter sicherer sind und es unwahrscheinlicher ist, dass sie kompromittiert oder gestohlen werden.

## Zugriff auf Teams und Repositorys einschränken

Um im Falle einer Sicherheitsverletzung die potenzielle Angriffsfläche zu begrenzen, sollten Sie Benutzern unbedingt nur den Zugriff auf Teams und Repositorys gewähren, den sie zum Erledigen ihrer Arbeit unbedingt benötigen. Da Mitglieder mit der Inhaberrolle auf alle Teams und Repositorys in der Organisation zugreifen können, wird dringend empfohlen, dieses Team möglichst klein zu halten.

For more information on configuring teams and team permissions, see "[Roles in an organization](/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization)."
