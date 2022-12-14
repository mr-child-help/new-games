---
title: Zugriffsberechtigungen auf GitHub
redirect_from:
  - /articles/needs-to-be-written-what-can-the-different-types-of-org-team-permissions-do/
  - /articles/what-are-the-different-types-of-team-permissions/
  - /articles/what-are-the-different-access-permissions/
  - /articles/access-permissions-on-github
  - /github/getting-started-with-github/access-permissions-on-github
  - /github/getting-started-with-github/learning-about-github/access-permissions-on-github
intro: 'Während Du Mitarbeitern in einem persönlichen Repository Lese-/Schreibzugriff gewähren kannst, können Mitglieder einer Organisation feiner abgestufte Zugriffsberechtigungen für die Repositorys der Organisation haben.'
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
topics:
  - Permissions
  - Accounts
shortTitle: Access permissions
---

## Persönliche Benutzerkonten

Ein Repository, das einem Benutzerkonto gehört, hat zwei Berechtigungsebenen: den *Repository-Inhaber* und *Mitarbeiter*. Weitere Informationen findest Du unter „[Berechtigungsebenen für ein Repository eines Benutzerkontos](/articles/permission-levels-for-a-user-account-repository)."

## Organisations-Konten

Organisationsmitglieder können folgende Rollen haben: *Inhaber*{% ifversion fpt or ghec %}, *Abrechnungsmanager*,{% endif %} oder *Mitglied*. Inhaber haben vollständigen administrativen Zugriff auf Deine Organisation{% ifversion fpt or ghec %}, wohingegen Abrechnungsmanager die Abrechnungseinstellungen verwalten können{% endif %}. Die Standardrolle für alle übrigen Personen lautet „Mitglied“. Du kannst die Zugriffsberechtigungen für mehrere Mitglieder gleichzeitig in Teams verwalten. Weitere Informationen findest Du unter:
- "[Roles in an organization](/organizations/managing-peoples-access-to-your-organization-with-roles/roles-in-an-organization)"
- „[Projektboardberechtigungen für eine Organisation](/articles/project-board-permissions-for-an-organization)“
- "[Repository roles for an organization](/organizations/managing-access-to-your-organizations-repositories/repository-roles-for-an-organization)"
- „[Informationen zu Teams](/articles/about-teams)“

{% ifversion fpt or ghec %}

## Enterprise-Konten

*Enterprise-Inhaber* haben die endgültige Kontrolle über das Enterprise-Konto und können sämtliche Aktionen im Enterprise-Konto durchführen. *Abrechnungsmanager* können die Abrechnungseinstellungen Deines Enterprise-Kontos verwalten. Mitglieder und externe Mitarbeiter von Organisationen im Besitz Deines Enterprise-Kontos sind automatisch Mitglieder des Enterprise-Kontos, aber sie haben keinen Zugriff auf das Enterprise-Konto selbst oder dessen Einstellungen. For more information, see "[Roles in an enterprise](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise)."

If an enterprise uses {% data variables.product.prodname_emus %}, members are provisioned as new user accounts on {% data variables.product.prodname_dotcom %} and are fully managed by the identity provider. The {% data variables.product.prodname_managed_users %} have read-only access to repositories that are not a part of their enterprise and cannot interact with users that are not also members of the enterprise. Within the organizations owned by the enterprise, the {% data variables.product.prodname_managed_users %} can be granted the same granular access levels available for regular organizations. For more information, see "[About {% data variables.product.prodname_emus %}]({% ifversion fpt %}/enterprise-cloud@latest{% endif %}/admin/authentication/managing-your-enterprise-users-with-your-identity-provider/about-enterprise-managed-users){% ifversion fpt %}" in the {% data variables.product.prodname_ghe_cloud %} documentation{% else %}."{% endif %}

{% data reusables.gated-features.enterprise-accounts %}

{% endif %}

## Weiterführende Informationen

- „[Arten von {% data variables.product.prodname_dotcom %}-Konten](/articles/types-of-github-accounts)“
