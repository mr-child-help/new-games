---
title: Selbst-gehostete Runner hinzufügen
intro: 'Du kannst einen selbst-gehosteten Runner zu {{ site.data.variables.product.prodname_actions }} hinzufügen.'
redirect_from:
  - /github/automating-your-workflow-with-github-actions/adding-self-hosted-runners
  - /actions/automating-your-workflow-with-github-actions/adding-self-hosted-runners
versions:
  fpt: '*'
  ghes: '*'
  ghae: '*'
  ghec: '*'
type: tutorial
shortTitle: Add self-hosted runners
---

{% data reusables.actions.ae-self-hosted-runners-notice %}
{% data reusables.actions.enterprise-beta %}
{% data reusables.actions.enterprise-github-hosted-runners %}
{% data reusables.actions.ae-beta %}

Du kannst einen selbst-gehosteten Runner zu {{ site.data.variables.product.prodname_actions }} hinzufügen.

If you are an organization or enterprise administrator, you might want to add your self-hosted runners at the organization or enterprise level. This approach makes the runner available to multiple repositories in your organization or enterprise, and also lets you to manage your runners in one place.

For information on supported operating systems for self-hosted runners, or using self-hosted runners with a proxy server, see "[About self-hosted runners](/github/automating-your-workflow-with-github-actions/about-self-hosted-runners)."

{% ifversion not ghae %}
{% warning %}

**Warning:** {% data reusables.github-actions.self-hosted-runner-security %}

Weitere Informationen findest Du unter „[Informationen zu selbst-gehosteten Runnern](/github/automating-your-workflow-with-github-actions/about-self-hosted-runners#self-hosted-runner-security-with-public-repositories)“.

{% endwarning %}
{% endif %}

## Einen selbst-gehosteten Runner zu einem Repository hinzufügen

Du kannst selbst-gehostete Runner zu einem einzigen Repository hinzufügen. To add a self-hosted runner to a user repository, you must be the repository owner. For an organization repository, you must be an organization owner or have admin access to the repository. For information about how to add a self-hosted runner with the REST API, see "[Self-hosted runners](/rest/reference/actions#self-hosted-runners)."

{% ifversion fpt or ghec %}
{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.github-actions.settings-sidebar-actions %}
{% data reusables.github-actions.settings-sidebar-actions-runners-updated %}
1. Click **New self-hosted runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}
{% ifversion ghae or ghes %}
{% data reusables.repositories.navigate-to-repo %}
{% data reusables.repositories.sidebar-settings %}
{% data reusables.github-actions.settings-sidebar-actions-runners %}
1. Under
{% ifversion fpt or ghes > 3.1 or ghae or ghec %}"Runners"{% else %}"Self-hosted runners"{% endif %}, click **Add runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}
{% data reusables.github-actions.self-hosted-runner-check-installation-success %}

## Einen selbst-gehosteten Runner zu einer Organisation hinzufügen

Du kannst selbst-gehostete Runner auf Organisationsebene hinzufügen, wo sie verwendet werden können, um Jobs für mehrere Repositories in einer Organisation zu verarbeiten. Um einen selbst-gehosteten Runner zu einer Organisation hinzuzufügen, musst Du Organisationsinhaber sein. For information about how to add a self-hosted runner with the REST API, see "[Self-hosted runners](/rest/reference/actions#self-hosted-runners)."

{% ifversion fpt or ghec %}
{% data reusables.organizations.navigate-to-org %}
{% data reusables.organizations.org_settings %}
{% data reusables.github-actions.settings-sidebar-actions %}
{% data reusables.github-actions.settings-sidebar-actions-runners-updated %}
1. Click **New runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}
{% ifversion ghae or ghes %}
{% data reusables.organizations.navigate-to-org %}
{% data reusables.organizations.org_settings %}
{% data reusables.github-actions.settings-sidebar-actions-runners %}
1. Under
{% ifversion fpt or ghes > 3.1 or ghae or ghec %}"Runners"{% else %}"Self-hosted runners"{% endif %}, click **Add runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}

{% data reusables.github-actions.self-hosted-runner-check-installation-success %}

{% data reusables.github-actions.self-hosted-runner-public-repo-access %}

## Adding a self-hosted runner to an enterprise

You can add self-hosted runners to an enterprise, where they can be assigned to multiple organizations. The organization admins are then able to control which repositories can use it.

New runners are assigned to the default group. You can modify the runner's group after you've registered the runner. For more information, see "[Managing access to self-hosted runners](/actions/hosting-your-own-runners/managing-access-to-self-hosted-runners-using-groups#moving-a-self-hosted-runner-to-a-group)."

{% ifversion fpt or ghec %}
To add a self-hosted runner to an enterprise account, you must be an enterprise owner. For information about how to add a self-hosted runner with the REST API, see the [Enterprise Administration GitHub Actions APIs](/rest/reference/enterprise-admin#github-actions).

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
{% data reusables.enterprise-accounts.actions-runners-tab %}
1. Click **New runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}
{% ifversion ghae or ghes %}
To add a self-hosted runner at the enterprise level of
{% data variables.product.product_location %}, you must be a site administrator.
{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.policies-tab %}
{% data reusables.enterprise-accounts.actions-tab %}
{% data reusables.enterprise-accounts.actions-runners-tab %}
1. Click **Add new**, then click **New runner**.
{% data reusables.github-actions.self-hosted-runner-configure %}
{% endif %}
{% data reusables.github-actions.self-hosted-runner-check-installation-success %}

{% data reusables.github-actions.self-hosted-runner-public-repo-access %}

### Making enterprise runners available to repositories

By default, runners in an enterprise's "Default" self-hosted runner group are available to all organizations in the enterprise, but are not available to all repositories in each organization.

To make an enterprise-level self-hosted runner group available to an organization repository, you might need to change the organization's inherited settings for the runner group to make the runner available to repositories in the organization.

For more information on changing runner group access settings, see "[Managing access to self-hosted runners using groups](/actions/hosting-your-own-runners/managing-access-to-self-hosted-runners-using-groups#changing-the-access-policy-of-a-self-hosted-runner-group)."
