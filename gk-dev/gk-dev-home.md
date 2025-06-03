---
title: GitKraken.dev Support Home
description: Learn how to work with gitkraken.dev features
taxonomy:
    category: gk-dev

---

<kbd>Last updated: June 2025</kbd>

GitKraken.dev is a web app that helps you stay on top of your projects. You can track issues and pull requests, work with your team, and manage repositories from your browser.

<figure>
  <img src="/wp-content/uploads/gkd-main-0.png" class="img-responsive center img-bordered help-center-img" alt="GitKraken.dev dashboard overview">
  <figcaption style="color:#888;text-align:center">GitKraken.dev dashboard overview</figcaption>
</figure>

***

## Launchpad

The Launchpad provides a summary of pull requests and issues relevant to your filters, allowing quick action. Instead of searching for these items individually, you get a comprehensive view of your tasks. Connect an [integration](/gk-dev/gk-dev-integrations/) to begin.

<div class='callout callout--warning'>
    <p>This feature is only available on Pro or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>


### Launchpad Actions

From the Launchpad, take actions on pull requests and issues via the actions column. Update fields, open branches in GitKraken Desktop or VS Code, merge or close pull requests, or open [code suggestions](/gk-dev/gk-dev-home/#code-suggest-pro).

<figure>
  <img src="/wp-content/uploads/gkd-take-action.png" class="img-bordered help-center-img" alt="Launchpad action options for PRs and issues">
  <figcaption style="color:#888;text-align:center">Launchpad action options for PRs and issues</figcaption>
</figure>

### Organizing the Launchpad

Use filters under the search bar to refine items shown. Select services, assigned/created/mentioned statuses, or filter further based on [workspaces](/gk-dev/gk-dev-home/#workspaces).

<figure>
  <img src="/wp-content/uploads/gkd-launchpad-filter.png" class="img-responsive center img-bordered help-center-img" alt="Launchpad filter options to refine visible items">
  <figcaption style="color:#888;text-align:center">Launchpad filter options to refine visible items</figcaption>
</figure>

Pin or snooze items for easier management. Click the pin icon to prioritize an item, or snooze it to hide under the SNOOZED section. Unsnooze items by revisiting the SNOOZED section.

<figure>
  <img src="/wp-content/uploads/gkd-pin-or-snooze.gif" class="img-responsive center img-bordered help-center-img" alt="GIF showing pinning and snoozing actions in Launchpad">
  <figcaption style="color:#888;text-align:center">Pin or snooze items to manage task visibility</figcaption>
</figure>

***

## Cloud Patches `PRO`

Cloud Patches are Git patches securely stored by GitKraken, accessible via GitKraken Desktop, GitLens, or the GitKraken CLI. Store patches securely or on your [AWS S3 bucket](/gk-dev/gk-dev-security-controls/#self-hosted) and collaborate early without a pull request.

<div class='callout callout--warning'>
    <p>This feature is only available on Pro or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>


### Creating a Cloud Patch

Create patches from [GitKraken Desktop](/gitkraken-client/experimental-features/#cloud-patches), [GitLens](gitlens/gitlens-features/#cloud-patches-preview), or [GitKraken CLI](/cli/cli-home/#cloud-patches). Manage shared Cloud Patches from gitkraken.dev.

<figure>
  <img src="/wp-content/uploads/gkd-cloud-patch-view.png" class="img-responsive center img-bordered help-center-img" alt="List of cloud patches in GitKraken.dev">
  <figcaption style="color:#888;text-align:center">Manage shared Cloud Patches from gitkraken.dev</figcaption>
</figure>

### Working with Cloud Patches

Select `Open` to view patch contents. Open in [GitKraken Desktop](/gitkraken-client/experimental-features/#cloud-patches) or [GitLens](gitlens/gitlens-features/#cloud-patches-preview) to apply patches.

<figure>
  <img src="/wp-content/uploads/gkd-open-cloud-patch.png" class="img-responsive center img-bordered help-center-img" alt="Open and review contents of a Cloud Patch">
  <figcaption style="color:#888;text-align:center">Review patch contents before applying</figcaption>
</figure>

***

## Workspaces

Group and share repositories with [teams](/gk-dev/gk-dev-organization/#teams) or organization members via GitKraken.dev, GitKraken Desktop, GitLens, or GitKraken CLI.

<figure>
  <img src="/wp-content/uploads/gkd-workspaces-view.png" class="img-bordered help-center-img" alt="Workspace list showing multiple repo groups">
  <figcaption style="color:#888;text-align:center">Manage grouped repositories in Workspaces</figcaption>
</figure>

### Creating a Workspace

Connect a [service integration](/gk-dev/gk-dev-integrations/), select `Create Workspace`, provide a name and provider, and optionally set a photo or share settings.

<figure>
  <img src="/wp-content/uploads/gkd-create-workspace.png" class="img-bordered help-center-img" style="max-height:600px;" alt="Create a new workspace modal">
  <figcaption style="color:#888;text-align:center">Create and customize a new Workspace</figcaption>
</figure>

### Working with Workspaces

Select `Open Launchpad` to filter by workspace. Use in GitKraken Desktop, GitLens, or GitKraken CLI to perform actions across repositories.

<figure>
  <img src="/wp-content/uploads/gkd-open-workspace.png" class="img-bordered help-center-img" alt="Open workspace to view associated repositories">
  <figcaption style="color:#888;text-align:center">Filter Launchpad and manage workspace repos</figcaption>
</figure>

### Requirement for Azure Workspaces and Insights

To use Workspaces and [Insights](/gk-dev/gk-dev-insights) with Azure, enable `Third-party application access via OAuth` in Azure's `Organization Settings > Policies`. [More details by Microsoft here](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

***

## Code Suggest `PRO`

GitKraken Code Suggest simplifies code review by letting you suggest edits across the project—not just changed lines—using GitKraken.dev, GitLens, or GitKraken Desktop. Suggestions are posted to the pull request for review and acceptance.

<figure>
  <img src="/wp-content/uploads/cli-code-suggest.png" class="img-bordered help-center-img" alt="Suggesting code changes within a pull request">
  <figcaption style="color:#888;text-align:center">Propose code changes across the project</figcaption>
</figure>

<div class='callout callout--warning'>
    <p>This feature is only available on Pro or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>


### Working with Code Suggestions

Create suggestions in [GitKraken Desktop](/gitkraken-client/pull-requests/#review-code-and-suggest-changes) or [GitLens](gitlens/gitlens-features/#code-suggest-preview).

Once submitted, the pull request includes a comment with links to open the suggestion in GitKraken.dev or on your machine.

<figure>
  <img src="/wp-content/uploads/gl-code-suggest-comment.png" class="img-bordered help-center-img" alt="PR comment with code suggestion options">
  <figcaption style="color:#888;text-align:center">Choose where to review code suggestions</figcaption>
</figure>

Select _Code Suggestion for #PR_ to open in GitKraken.dev and review the changes. Accepting adds a commit to the remote branch.

<figure>
  <img src="/wp-content/uploads/gl-accept-code-suggestion.gif" class="img-bordered help-center-img" alt="GIF showing how to accept a code suggestion">
  <figcaption style="color:#888;text-align:center">Review and accept code suggestions in GitKraken.dev</figcaption>
</figure>
