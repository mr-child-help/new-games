---
title: Viewing people in your enterprise
intro: 'To audit access to enterprise-owned resources or user license usage, enterprise owners can view every administrator and member of the enterprise.'
product: '{% data reusables.gated-features.enterprise-accounts %}'
redirect_from:
  - /github/setting-up-and-managing-your-enterprise-account/viewing-people-in-your-enterprise-account
  - /articles/viewing-people-in-your-enterprise-account
  - /github/setting-up-and-managing-your-enterprise/viewing-people-in-your-enterprise
  - /github/setting-up-and-managing-your-enterprise/managing-users-in-your-enterprise/viewing-people-in-your-enterprise
versions:
  ghec: '*'
  ghes: '*'
  ghae: '*'
topics:
  - Enterprise
shortTitle: View people in your enterprise
---

## Viewing enterprise owners{% ifversion ghec %} and billing managers{% endif %}

You can view enterprise owners {% ifversion ghec %} and billing managers, {% endif %}as well as a list of pending invitations to become owners{% ifversion ghec %} and billing managers. You can filter the list of enterprise administrators by role{% endif %}. Du kannst eine bestimmte Person nach ihrem Benutzernamen oder vollständigen Namen suchen.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
{% data reusables.enterprise-accounts.administrators-tab %}
{% ifversion ghec %}1. Optionally, to view a list of pending invitations, click **_NUMBER_ pending**.
  !["NUMBER pending" button to the right of search and filter options](/assets/images/help/enterprises/administrators-pending.png){% endif %}

## Mitglieder und externe Mitarbeiter anzeigen

Du kannst die Anzahl der ausstehenden Mitglieder und externen Mitarbeiter anzeigen. You can filter the list of members by {% ifversion ghec %}deployment ({% data variables.product.prodname_ghe_cloud %} or {% data variables.product.prodname_ghe_server %}),{% endif %} role{% ifversion ghec %}, and{% else %} or {% endif %} organization. Du kannst die Liste der externen Mitarbeiter nach der Sichtbarkeit der Repositorys filtern, auf die der Mitarbeiter zugreifen kann. Du kannst eine bestimmte Person nach ihrem Benutzernamen oder Anzeigenamen suchen.

You can view {% ifversion ghec %}all the {% data variables.product.prodname_ghe_cloud %} organizations and {% data variables.product.prodname_ghe_server %} instances that a member belongs to, and {% endif %}which repositories an outside collaborator has access to{% ifversion ghec %}, {% endif %} by clicking on the person's name.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
1. Wenn Du optional anstelle der Liste der Mitglieder eine Liste der externen Mitarbeiter anzeigen möchtest, klicke auf **Outside collaborators** (Externe Mitarbeiter). ![Registerkarte „Outside collaborators“ (Externe Mitarbeiter) auf der Seite „Organization members“ (Organisationsmitglieder)](/assets/images/help/business-accounts/outside-collaborators-tab.png)
{% ifversion ghec %}1. Optionally, to view a list of pending invitations, click **_NUMBER_ pending**.
  !["NUMBER pending" button to the right of search and filter options](/assets/images/help/enterprises/members-pending.png){% endif %}

## Weiterführende Informationen

- "[Roles in an enterprise](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise)"
