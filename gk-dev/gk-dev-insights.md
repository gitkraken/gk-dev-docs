---
title: Insights
description: GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories. It provides a visual representation of your repository's history, allowing you to see how your codebase has evolved over time. This data can help you make informed decisions and optimize your workflow.

Insights is available for GitHub.com, Bitbucket.org, GitLab.com, and Azure DevOps (Hosted).

<figure>
  <img src="/wp-content/uploads/gkdev-insights.png" srcset="/wp-content/uploads/gkdev-insights@2x.png" class="img-bordered center help-center-img" alt="Graph view of pull request activity over time in GitKraken Insights">
  <figcaption style="color:#888;text-align:center">Visualize pull request activity across your repositories</figcaption>
</figure>

<div class='callout callout--warning'>
  <p>
    <strong>Preview Mode:</strong> Insights is in Preview. Click the "Feedback" button in the top right to share your thoughts with us.
  </p>
</div>

***

## How do I use GitKraken Insights?

Access Insights at [gitkraken.dev/insights](https://gitkraken.dev/insights?source=help_center).

To get started:

1. [Connect an integration](/gk-dev/gk-dev-integrations/) at [gitkraken.dev/settings/integrations](https://gitkraken.dev/settings/integrations?source=help_center)
2. Create a [Cloud Workspace](/gk-dev/gk-dev-home/#workspaces) at [gitkraken.dev/workspaces](https://gitkraken.dev/workspaces?source=help_center)

Once both are set up, you can filter by workspace and date range to view Insights metrics for those repositories.

<figure>
  <img src="/wp-content/uploads/gkdev-insights-filters.png" srcset="/wp-content/uploads/gkdev-insights-filters@2x.png" class="img-bordered center help-center-img" alt="Filters available for GitKraken Insights by workspace and date">
  <figcaption style="color:#888;text-align:center">Filter Insights by workspace and timeframe</figcaption>
</figure>

<div class='callout callout--note'>
  <p>
    GitKraken attempts to add webhooks to your workspace repositories to reduce API calls and enhance data performance.
  </p>
  <p>
    14-day filtering is available on Teams plans; 28-day filtering is available on Enterprise plans.
  </p>
</div>

### Requirement for Azure Insights and Workspaces

To use Insights and [Workspaces](/gk-dev/gk-dev-home/#workspaces) with Azure, ensure `Third-party application access via OAuth` is enabled in Azure under `Organization Settings > Policies`. [Learn more](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

***

## Metrics

GitKraken Insights offers the following metrics. Hover over the <i class="fa-solid fa-circle-info"></i> icon in-app to see detailed descriptions.

* **Cycle Time** – Average time to merge a pull request within the selected period.
* **Average Throughput** – Number of pull requests merged in the selected period.
* **Merge Rate** – Percentage of merged pull requests compared to all open pull requests.
* **Open** – Total pull requests opened during the selected period.
* **Merged** – Total pull requests merged during the selected period.

***

## Export Insights Data

You can export Insights data as a CSV by selecting **Export CSV** in the top right corner of the screen.

<figure>
  <img src="/wp-content/uploads/gkdev-insights-export.png" srcset="/wp-content/uploads/gkdev-insights-export@2x.png" class="img-bordered center help-center-img" alt="CSV export option in GitKraken Insights">
  <figcaption style="color:#888;text-align:center">Export GitKraken Insights data as a CSV</figcaption>
</figure>

<div class='callout callout--note'>
  <p><strong>Note:</strong> Exporting is only available for Enterprise subscriptions.</p>
</div>
