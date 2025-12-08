---
title: Automations
description: Learn how to use GitKraken.dev automations to streamline GitHub, Bitbucket, Azure DevOps and GitLab workflows with triggers, conditions, and actions.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: December 2025</kbd>

Use **GitKraken.dev Automations** to create rule-based workflows that trigger actions when pull requests and issues match specific conditions. Automations help you streamline collaboration and enforce consistency across teams.


<div class='callout callout--warning'>
    <p>This feature is only available on Pro subscription tiers or higher. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>

***

## Automation examples

Here are a few ways teams are using Automations to reduce manual effort and create scalable workflows:

- **Safe deployments**: Add a checklist for database migrations.
- **Critical code reviews**: Assign reviewers to high-impact areas like payments.
- **Security checks**: Flag sensitive changes (e.g., auth) for review.
- **Refactoring guardrails**: Prevent conflicts and schedule follow-ups.
- **SOC 2 compliance**: Automate tasks for encryption and security checks.
- **DevOps enhancements**: Enforce quality checks and automate infrastructure changes.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Automations currently supports cloud integrations. Self-hosted support will be added in a future update.</p>
</div>

***

## Get started with automations

Log in at [gitkraken.dev](https://gitkraken.dev/?source=help_center&product=gitkraken_dot_dev) and select **Automations** in the left menu. If it's your first time, you'll see the get started page with the option to create a new automation or use a suggested template.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations.jpeg" class="help-center-img img-bordered" alt="Automations landing page in GitKraken.dev">
  <figcaption style="color:#888;text-align:center">Automations landing page on GitKraken.dev</figcaption>
</figure>

### Create an automation

Click <button class="button button--success button--ui button--nolink">+ Create Automation</button>.

1. Name your automation.
2. Choose from the Provider dropdown.
3. Pick the target repository.
4. (Optional) Enable for draft pull requests by checking the box.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations2.png" class="help-center-img img-bordered" alt="Form to create a new automation rule">
  <figcaption style="color:#888;text-align:center">Setup form for new automation</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Creating an automation sets up a webhook on the repository. You’ll need the appropriate permissions.</p>
</div>

***


## Set Conditions

Conditions define when an automation is triggered. GitKraken currently supports the following condition types:

- **Pull request content**  
  Trigger on PR metadata, activity, or discussion.

- **Review: Status**  
  Watch for approvals, missing reviews, or stale feedback.

- **Branch and origin**  
  Trigger based on the source or target branch, or the repository.

- **CI/CD checks**  
  React to build, test, and deployment outcomes.

- **File condition**  
  Match file paths, folders, or specific code snippets.

- **GitKraken AI**  
  Analyze pull request diffs and metadata to detect conditions you care about.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations3.png" class="help-center-img img-bordered" alt="Conditions configuration screen">
  <figcaption style="color:#888;text-align:center">Set up condition rules for triggering actions</figcaption>
</figure>

### Boolean logic

You can choose whether **all** or **any** of the conditions must be true.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations4.png" class="help-center-img img-bordered" alt="Boolean logic options for condition matching">
  <figcaption style="color:#888;text-align:center">Select logic to match all or any conditions</figcaption>
</figure>

### File location conditions

- **File name**: Matches file names.
- **File path**: Matches full file paths.
- **File added in folder**: Triggers when a new file is added to a specified folder in a PR.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> A file path includes folders, e.g. <code>src/app/index.ts</code>, while a file name is just <code>index.ts</code>.</p>
</div>

### File contents conditions

- **Old code**: Matches the red (left side) of a split diff.
- **New code**: Matches the green (right side) of a split diff.
- **New and old code**: Matches both sides.

### Pull request conditions

- **Number of changed files**
- **PR author**
- **PR labels**


## Actions

GitKraken supports these automation actions:

### AI

- **GitKraken AI**  
  Post a comment with a summary generated from an AI prompt.

### People

- **Notify user**  
  Send a custom notification to selected users.

- **Add reviewer**  
  Assign a reviewer or team, with an optional message.

- **Add assignee**  
  Assign the PR to selected users, optionally including a message.

- **Remove reviewer**  
  Unassign a reviewer or team from the PR.

- **Remove assignee**  
  Unassign a user from the PR.

### Pull Request

- **Add comment**  
  Post a comment on the PR.

- **Add label**  
  Apply a GitHub label to the PR.

- **Close PR**  
  Automatically close the pull request.

- **Add to checklist**  
  Add checklist items to the PR description.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Authors can’t review their own PRs. If selected, GitKraken will skip that step and apply all others.</p>
</div>

***

## Manage saved automations

Once you've created automations, manage them at [GitKraken.dev](https://gitkraken.dev/automations/general?source=help_center&product=gitkraken_dot_dev).

You can:

- Enable/disable
- Edit
- Delete
- Duplicate
- Sort by status or action

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations5.png" class="help-center-img img-bordered" alt="List of saved automations">
  <figcaption style="color:#888;text-align:center">Manage and organize saved automations</figcaption>
</figure>

### Edit, delete, or duplicate

Use the <i class="fas fa-ellipsis-v"></i> icon next to an automation name.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations6.png" class="help-center-img img-bordered" alt="Automation options menu">
  <figcaption style="color:#888;text-align:center">Automation menu with edit, delete, and duplicate options</figcaption>
</figure>

### Sort automations

Sort by **Status** (enabled/disabled) or **Action** (type of triggered automation).

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations7.png" class="help-center-img img-bordered" alt="Sorting automations by status or action">
  <figcaption style="color:#888;text-align:center">Sort saved automations by different criteria</figcaption>
</figure>

### Add another automation

Click <button class="button button--success button--ui button--nolink">+ Create Automation</button> again from the list view.

***

## Repository management

The Repository Management screen shows which repos have active automations, who created them, the provider, and automation counts.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations8.png" class="help-center-img img-bordered" alt="Repository automation overview">
  <figcaption style="color:#888;text-align:center">View repository-level automation status</figcaption>
</figure>

Admins can also add/remove repos or perform bulk actions.

<figure>
  <img src="/wp-content/uploads/gkdev-createautomations9.png" class="help-center-img img-bordered" alt="Repository admin tasks for automations">
  <figcaption style="color:#888;text-align:center">Admin view for managing repository automation</figcaption>
</figure>

***

## Next Steps

Explore more ways to automate and streamline Git workflows:
- [Connect an Integration](/gk-dev/gk-dev-integrations/)
- [Use Launchpad to manage PRs and issues](/gk-dev/gk-dev-home/#launchpad-your-daily-git-dashboard)
- [Visualize metrics with GitKraken Insights](/gk-dev/gk-dev-insights/)
- [Return to GitKraken.dev Support Home](/gk-dev/gk-dev-home/)