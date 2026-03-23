---
title: Automations
description: Learn how to use GitKraken.dev automations to streamline GitHub, Bitbucket, Azure DevOps and GitLab workflows with triggers, conditions, and actions.
product: "GitKraken.dev"
content_type: "how-to"
audience: "developer"
plan_required: "Advanced, Business, Enterprise"
cloud_only: true
status: "GA"
last_verified: "2026-03"
taxonomy:
    category: gk-dev
---

<kbd>Last updated: March 2026</kbd>

Use **GitKraken.dev Automations** to create rule-based workflows that trigger actions when pull requests and issues match specific conditions. Automations help you streamline collaboration and enforce consistency across teams.


<div class='callout callout--warning'>
    <p>This feature is only available on Advanced or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>

***

## Quick Start

GitKraken.dev Automations trigger configured actions on pull requests and issues when defined conditions are met. Automations require an Advanced or higher subscription and support cloud integrations only.

To create an automation:

1. Sign in at [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken_dot_dev) and select **Automations** from the left sidebar.
2. Click **+ Create Automation**, enter a name, select a Git provider, and choose a target repository. This installs a webhook on the repository.
3. Under **Conditions**, add one or more triggers: pull request content, review status, branch, CI/CD outcome, file path, or GitKraken AI analysis.
4. Set the condition logic to **All** or **Any**.
5. Under **Actions**, configure the response: notify users, add or remove reviewers or assignees, post a comment, apply a label, close the PR, or add checklist items.
6. Save and enable the automation.

From the Automations list view, automations can be enabled, disabled, duplicated, or deleted individually.

***

## When to use automations

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

Conditions define when an automation is triggered. Requires Owner or Admin role to create or edit automations.

| Condition Type | Triggers On | Example |
|---|---|---|
| Pull request content | PR metadata, activity, or discussion | PR title contains "hotfix" |
| Review: Status | Approvals, missing reviews, or stale feedback | PR has no reviews after 24 hours |
| Branch and origin | Source or target branch, or repository | Target branch is `main` |
| CI/CD checks | Build, test, and deployment outcomes | CI pipeline fails |
| File condition | File paths, folders, or code snippets | File path matches `src/auth/*` |
| GitKraken AI | AI analysis of PR diffs and metadata | AI detects security-sensitive changes |

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


## What actions can an automation perform?

GitKraken supports these automation actions:

| Action | Category | Effect |
|---|---|---|
| GitKraken AI | AI | Posts an AI-generated summary comment on the PR |
| Notify user | People | Sends a custom notification to selected users |
| Add reviewer | People | Assigns a reviewer or team, with an optional message |
| Add assignee | People | Assigns the PR to selected users |
| Remove reviewer | People | Unassigns a reviewer or team from the PR |
| Remove assignee | People | Unassigns a user from the PR |
| Add comment | Pull Request | Posts a comment on the PR |
| Add label | Pull Request | Applies a GitHub label to the PR |
| Close PR | Pull Request | Closes the pull request |
| Add to checklist | Pull Request | Adds checklist items to the PR description |

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

## How to manage repositories with automations

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