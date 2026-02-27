---
title: Connect GitHub, GitLab, Azure Integrations
description: Step-by-step guide to connecting GitHub, GitLab, Bitbucket, and self-hosted integrations on GitKraken.dev for Launchpad, Insights, Workspaces, and Cloud Patches.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: February 2026</kbd>

Connect integrations on GitKraken.dev to use features like Launchpad, Workspaces, and Cloud Patches. Supported integrations include GitHub, GitLab, Bitbucket, Azure DevOps, and self-hosted options.

***

## How to Connect an Integration

Go to the <a href="https://gitkraken.dev/settings/integrations?source=help_center&product=gitkraken_dot_dev" target="_blank">Integrations page</a> in GitKraken.dev and follow the instructions based on the type of integration.

### 1. Cloud-Based Integrations (GitHub, GitLab.com, Bitbucket.org, Azure DevOps)

1. Under **Add Integration**, select your service.
2. Log into your account.
3. Approve access when prompted to authorize GitKraken.

### 2. Self-Hosted or Server-Based Integrations

1. Under **Add Integration**, select your self-hosted service (e.g., GitHub Enterprise).
2. Enter the Host Domain.
3. Click **Generate a token on {service}**.
   - This opens a pre-filled Personal Access Token (PAT) creation page.
4. Create the PAT.
5. Paste the token into GitKraken.
6. Click **Connect**.

<figure>
  <img src="/wp-content/uploads/gkd-integrations-0.png" class="center img-bordered help-center-img" alt="Connecting GitHub and GitLab integrations in GitKraken.dev">
  <figcaption style="color:#888;text-align:center">Integration settings page on GitKraken.dev</figcaption>
</figure>

<div class='callout callout--basic'>
    <p>To access repositories owned by a GitHub organization, organization approval is required. <a href="https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/" target="_blank">Request organization approval</a>.</p>
</div>

***

## What’s Next?

Once connected, you can:
- Use [Launchpad](/gk-dev/gk-dev-home/#launchpad-your-daily-git-dashboard) to track PRs and issues.
- Organize repos into [Workspaces](/gk-dev/gk-dev-home/#workspaces-organize-projects-by-team).
- Share [Cloud Patches](/gk-dev/gk-dev-home/#create-and-share-cloud-patches).

Return to the [GitKraken.dev Support Home](/gk-dev/gk-dev-home/) to explore more features.
