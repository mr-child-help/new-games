---
title: Quickstart for projects (beta)
intro: 'Experience the speed, flexibility, and customization of projects (beta) by creating a project in this interactive guide.'
allowTitleToDifferFromFilename: true
miniTocMaxHeadingLevel: 3
versions:
  fpt: '*'
  ghec: '*'
type: quick_start
topics:
  - Projects
---

{% data reusables.projects.projects-beta %}

## Einführung

This guide demonstrates how to use projects (beta) to plan and track work. In this guide, you will create a new project and add a custom field to track priorities for your tasks. You'll also learn how to create saved views that help you communicate priorities and progress with your collaborators.

## Vorrausetzungen

You can either create an organization project or a user project. To create an organization project, you need a {% data variables.product.prodname_dotcom %} organization. For more information about creating an organization, see "[Creating a new organization from scratch](/organizations/collaborating-with-groups-in-organizations/creating-a-new-organization-from-scratch)."

In this guide, you will add existing issues from repositories owned by your organization (for organization projects) or by you (for user projects) to your new project. For more information about creating issues, see "[Creating an issue](/issues/tracking-your-work-with-issues/creating-an-issue)."

## Creating a project

First, create an organization project or a user project.

### Creating an organization project

{% data reusables.projects.create-project %}

### Creating a user project

{% data reusables.projects.create-user-project %}

## Adding issues to your project

Next, add a few issues to your project.

When your new project initializes, it prompts you to add items to your project. If you lose this view or want to add more issues later, place your cursor in the bottom row of the project, next to the {% octicon "plus" aria-label="plus icon" %}.

1. Type `#`.
2. Select the repository where your issue is located. To narrow down the options, you can start typing a part of the repository name.
3. Select your issue. To narrow down the options, you can start typing a part of the issue title.

Repeat the above steps a few times to add multiple issues to your project.

For more information about other ways to add issues to your project, or about other items you can add to your project, see "[Creating a project](/issues/trying-out-the-new-projects-experience/creating-a-project#adding-items-to-your-project)."

## Creating a field to track priority

Now, create a custom field called `Priority` to contain the values: `High`, `Medium`, or `Low`.

1. {% data reusables.projects.open-command-palette %}
2. Start typing any part of "Create new field".
3. Select **Create new field**.
4. In the resulting pop-up, enter `Priority` in the text box.
5. In the drop-down, select **Single select**.
6. Add options for `High`, `Medium`, and `Low`. You can also include emojis in your options. ![New single select field example](/assets/images/help/projects/new-single-select-field.png)
7. Klicke auf **Save** (Speichern).

Specify a priority for all issues in your project.

![Example priorities](/assets/images/help/projects/priority_example.png)

## Grouping issues by priority

Next, group all of the items in your project by priority to make it easier to focus on the high priority items.

1. {% data reusables.projects.open-command-palette %}
2. Start typing any part of "Group by".
3. Select **Group by: Priority**.

Now, move issues between groups to change their priority.

1. Choose an issue.
2. Drag and drop the issue into a different priority group. When you do this, the priority of the issue will change to be the priority of its new group.

![Move issue between groups](/assets/images/help/projects/move_between_group.gif)

## Saving the priority view

When you grouped your issues by priority in the previous step, your project displayed an indicator to show that the view was modified. Save these changes so that your collaborators will also see the tasks grouped by priority.

1. Select the drop-down menu next to the view name.
2. Klicke auf **Save changes** (Änderungen speichern).

To indicate the purpose of the view, give it a descriptive name.

1. Place your cursor in the current view name, **View 1**.
2. Replace the existing text with the new name, `Priorities`.

You can share the URL with your team to keep everyone aligned on the project priorities.

When a view is saved, anyone who opens the project will see the saved view. Here, you grouped by priority, but you can also add other modifiers such as sort, filter, or layout. Next, you will create a new view with the layout modified.

## Adding a board layout

To view the progress of your project's issues, you can switch to board layout.

The board layout is based on the status field, so specify a status for each issue in your project.

![Example status](/assets/images/help/projects/status_example.png)

Then, create a new view.

1. Click {% octicon "plus" aria-label="the plus icon" %} **New view** next to the rightmost view.

Next, switch to board layout.

1. {% data reusables.projects.open-command-palette %}
2. Start typing any part of "Switch layout: Board".
3. Select **Switch layout: Board**. ![Example priorities](/assets/images/help/projects/example_board.png)

When you changed the layout, your project displayed an indicator to show that the view was modified. Save this view so that you and your collaborators can easily access it in the future.

1. Select the drop-down menu next to the view name.
2. Klicke auf **Save changes** (Änderungen speichern).

To indicate the purpose of the view, give it a descriptive name.

1. Place your cursor in the current view name, **View 2**.
2. Replace the existing text with the new name, `Progress`.

![Example priorities](/assets/images/help/projects/project-view-switch.gif)

## Configure built-in automation

Finally, add a built in workflow to set the status to **Todo** when an item is added to your project.

1. In your project, click {% octicon "workflow" aria-label="the workflow icon" %}.
2. Under **Default workflows**, click **Item added to project**.
3. Next to **When**, ensure that both `issues` and `pull requests` are selected.
4. Next to **Set**, select **Status:Todo**.
5. Click the **Disabled** toggle to enable the workflow.

## Nächste Schritte:

You can use projects for a wide range of purposes. Ein Beispiel:

- Track work for a release
- Plan a sprint
- Prioritize a backlog

Here are some helpful resources for taking your next steps with {% data variables.product.prodname_github_issues %}:

- To provide feedback about the projects (beta) experience, go to the [GitHub feedback repository](https://github.com/github/feedback/discussions/categories/issues-feedback).
- To learn more about how projects can help you with planning and tracking, see "[About projects](/issues/trying-out-the-new-projects-experience/about-projects)."
- To learn more about the fields and items you can add to your project, see "[Creating a project](/issues/trying-out-the-new-projects-experience/creating-a-project)."
- To learn about more ways to display the information you need, see "[Customizing your project views](/issues/trying-out-the-new-projects-experience/customizing-your-project-views)."
