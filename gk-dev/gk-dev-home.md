---
title: GitKraken.dev Support Home
description: Learn how to work with GitKraken.dev features including Launchpad, Cloud Patches, Workspaces, and Code Suggestions.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

GitKraken.dev is a browser-based Git project management app. From tracking issues and pull requests to organizing repositories with your team, GitKraken.dev helps you stay productive directly from your browser.

<figure>
  <img src="/wp-content/uploads/gkd-main-0.png" class="img-responsive center img-bordered help-center-img" alt="GitKraken.dev dashboard overview">
  <figcaption style="color:#888;text-align:center">Overview of the GitKraken.dev dashboard</figcaption>
</figure>

***

## Launchpad: Your Daily Git Dashboard

The Launchpad offers a real-time summary of pull requests and issues based on your filters, helping you take action faster without context-switching.

Connect an [integration](/gk-dev/gk-dev-integrations/) to begin.

<div class='callout callout--warning'>
    <p>This feature is only available on Pro or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>

### Take Quick Actions from Launchpad

Use the actions column to update fields, open branches in GitKraken Desktop or VS Code, merge or close pull requests, and open [code suggestions](/gk-dev/gk-dev-home/#code-suggest-pro).

<figure>
  <img src="/wp-content/uploads/gkd-take-action.png" class="img-bordered help-center-img" alt="Launchpad action options for PRs and issues">
  <figcaption style="color:#888;text-align:center">Quick actions available for pull requests and issues</figcaption>
</figure>

### Refine Results with Filters

Filter the Launchpad by services, statuses (assigned/created/mentioned), or [workspaces](/gk-dev/gk-dev-home/#workspaces).

<figure>
  <img src="/wp-content/uploads/gkd-launchpad-filter.png" class="img-responsive center img-bordered help-center-img" alt="Launchpad filter options to refine visible items">
  <figcaption style="color:#888;text-align:center">Use filters to narrow down visible tasks</figcaption>
</figure>

Pin items for priority or snooze them to hide under the SNOOZED section. Return to the SNOOZED section to unsnooze.

<figure>
  <img src="/wp-content/uploads/gkd-pin-or-snooze.gif" class="img-responsive center img-bordered help-center-img" alt="GIF showing pinning and snoozing actions in Launchpad">
  <figcaption style="color:#888;text-align:center">Pin or snooze tasks for focused attention</figcaption>
</figure>

***

## Cloud Patches `PRO`

Cloud Patches let you securely store and share Git patches without a pull request. Create them using GitKraken Desktop, GitLens, or the GitKraken CLI. Store them on GitKraken servers or your own [AWS S3 bucket](/gk-dev/gk-dev-security-controls/#self-hosted).

<div class='callout callout--warning'>
    <p>This feature is only available on Pro or higher plans. <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken_dot_dev" target="_blank">See pricing options</a>.</p>
</div>

### Create and Share Cloud Patches

Initiate patches from [GitKraken Desktop](/gitkraken-client/experimental-features/#cloud-patches), [GitLens](gitlens/gitlens-features/#cloud-patches-preview), or [GitKraken CLI](/cli/cli-home/#cloud-patches). Manage shared Cloud Patches from gitkraken.dev.

<figure>
  <img src="/wp-content/uploads/gkd-cloud-patch-view.png" class="img-responsive center img-bordered help-center-img" alt="List of cloud patches in GitKraken.dev">
  <figcaption style="color:#888;text-align:center">View and manage shared Cloud Patches</figcaption>
</figure>

### Apply and Review Patches

Select `Open` to view patch contents. Open patches in GitKraken Desktop or GitLens to apply them.

<figure>
  <img src="/wp-content/uploads/gkd-open-cloud-patch.png" class="img-responsive center img-bordered help-center-img" alt="Open and review contents of a Cloud Patch">
  <figcaption style="color:#888;text-align:center">Review patch details before applying</figcaption>
</figure>

***

## Workspaces: Organize Projects by Team

Use Workspaces to group repositories for teams or organizations using GitKraken.dev, GitKraken Desktop, GitLens, or GitKraken CLI.

<figure>
  <img src="/wp-content/uploads/gkd-workspaces-view.png" class="img-bordered help-center-img" alt="Workspace list showing multiple repo groups">
  <figcaption style="color:#888;text-align:center">Group repositories under shared Workspaces</figcaption>
</figure>

### Set Up a New Workspace

Connect a [service integration](/gk-dev/gk-dev-integrations/), select `Create Workspace`, name it, choose a provider, and set sharing preferences.

<figure>
  <img src="/wp-content/uploads/gkd-create-workspace.png" class="img-bordered help-center-img" style="max-height:600px;" alt="Create a new workspace modal">
  <figcaption style="color:#888;text-align:center">Customize your Workspace with settings and visuals</figcaption>
</figure>

### Use Workspaces Across Tools

Click `Open Launchpad` to focus on that Workspace’s repositories. Perform Git actions in your preferred GitKraken tool.

<figure>
  <img src="/wp-content/uploads/gkd-open-workspace.png" class="img-bordered help-center-img" alt="Open workspace to view associated repositories">
  <figcaption style="color:#888;text-align:center">Work across repositories from a single Workspace</figcaption>
</figure>

### Azure Configuration for Workspaces & Insights

To use Workspaces or [Insights](/gk-dev/gk-dev-insights) with Azure DevOps, enable `Third-party application access via OAuth` in Azure’s Organization Settings. [Learn more from Microsoft](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

***

## Code Suggest `PRO`

Suggest code edits across your codebase—not just changed lines—using GitKraken.dev, GitLens, or GitKraken Desktop. Suggestions appear in the pull request for review.

<figure>
  <img src="/wp-content/uploads/cli-code-suggest.png" class="img-bordered help-center-img" alt="Suggesting code changes within a pull request">
  <figcaption style="color:#888;text-align:center">Post suggested edits across your project</figcaption>
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

***

## Next Steps

Explore more GitKraken.dev documentation:
- [Integrations](/gk-dev/gk-dev-integrations/)
- [Organization Management](/gk-dev/gk-dev-organization/)
- [Security Controls](/gk-dev/gk-dev-security-controls/)
- [Insights](/gk-dev/gk-dev-insights/)
