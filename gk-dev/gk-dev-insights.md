---
title: GitKraken Insights | PR Analytics Dashboard 
description: Use GitKraken Insights to analyze pull request metrics like cycle time, merge rate, and throughput with a visual dashboard.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

<div style="background-color: #fff8e1; border-left: 4px solid #fbc02d; padding: 12px; margin-bottom: 24px; color: #000;">
  <strong>Heads up:</strong> We're excited to launch the new GitKraken Insights soon! The current version will be retired at that time. Stay tuned for more details.
</div>

GitKraken Insights is an interactive analytics dashboard that visualizes how pull requests are merged across your repositories. Use it to track contribution velocity, monitor merge patterns, and evaluate engineering efficiency over time.

<figure>
  <img src="/wp-content/uploads/gkdev-insights.png" srcset="/wp-content/uploads/gkdev-insights@2x.png" class="img-bordered center help-center-img" alt="Graph of PR trends in GitKraken Insights">
  <figcaption style="color:#888;text-align:center">Visualize pull request activity across your repositories</figcaption>
</figure>

<div class='callout callout--warning'>
  <p><strong>Preview Mode:</strong> Insights is in Preview. Click the "Feedback" button in the top right to share your thoughts with us.</p>
</div>

***

## How to Get Started

Access Insights at [gitkraken.dev/insights](https://gitkraken.dev/insights?source=help_center).

1. [Connect an integration](/gk-dev/gk-dev-integrations/) at [gitkraken.dev/settings/integrations](https://gitkraken.dev/settings/integrations?source=help_center)
2. Create a [Cloud Workspace](/gk-dev/gk-dev-home/#workspaces) at [gitkraken.dev/workspaces](https://gitkraken.dev/workspaces?source=help_center)

Once set up, filter by workspace and date to explore pull request data.

<figure>
  <img src="/wp-content/uploads/gkdev-insights-filters.png" srcset="/wp-content/uploads/gkdev-insights-filters@2x.png" class="img-bordered center help-center-img" alt="Filter controls in GitKraken Insights dashboard">
  <figcaption style="color:#888;text-align:center">Filter Insights by workspace and timeframe</figcaption>
</figure>

<div class='callout callout--note'>
  <p>GitKraken attempts to add webhooks to your workspace repositories to reduce API calls and improve data freshness.</p>
  <p>14-day filtering is available on Teams plans; 28-day filtering is available on Enterprise plans.</p>
</div>

### Azure DevOps Requirements

To use Insights and [Workspaces](/gk-dev/gk-dev-home/#workspaces) with Azure, enable `Third-party application access via OAuth` under Azure’s `Organization Settings > Policies`. [Learn more](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

***

## Insights Metrics Explained

The dashboard surfaces actionable pull request metrics to help identify trends and blockers for the selected period of time:

- **Cycle Time** – Average time to merge a pull request.
- **Average Throughput** – Total number of pull requests merged.
- **Merge Rate** – Ratio of merged pull requests to total open.
- **Open** – Number of pull requests opened.
- **Merged** – Number of pull requests successfully merged.

Hover over the <i class="fa-solid fa-circle-info"></i> icons in-app to see detailed definitions.

***

## Export Your Data

Insights data can be exported as a CSV file.

1. Click **Export CSV** in the top right of the dashboard.
2. Download and analyze data externally.

<figure>
  <img src="/wp-content/uploads/gkdev-insights-export.png" srcset="/wp-content/uploads/gkdev-insights-export@2x.png" class="img-bordered center help-center-img" alt="Export button in GitKraken Insights">
  <figcaption style="color:#888;text-align:center">Export GitKraken Insights data as a CSV</figcaption>
</figure>

<div class='callout callout--note'>
  <p><strong>Note:</strong> Exporting is only available for Enterprise subscriptions.</p>
</div>

***

## Next Steps

Continue exploring GitKraken.dev analytics and collaboration features:
- [Connect an Integration](/gk-dev/gk-dev-integrations/)
- [Set up a Workspace](/gk-dev/gk-dev-home/#workspaces-organize-projects-by-team)
- [Learn about Launchpad](/gk-dev/gk-dev-home/#launchpad-your-daily-git-dashboard)
- [Visit GitKraken.dev Support Home](/gk-dev/gk-dev-home/)
