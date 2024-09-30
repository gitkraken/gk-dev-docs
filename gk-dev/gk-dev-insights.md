---

title: Insights
description: GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories.
taxonomy:
    category: gk-dev

---

GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories. It provides a visual representation of your repository's history, allowing you to see how your codebase has evolved over time. You can use this information to make informed decisions about how to improve your workflow.

Insights is available for Github.com, Bitbucket.org, Gitlab.com, and Azure DevOps (Hosted).

<img src="/wp-content/uploads/gkdev-insights.png" srcset="/wp-content/uploads/gkdev-insights@2x.png" class="img-bordered img-responsive center">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong> Insights is in Preview mode, and we'd love to hear your thoughts and feedback. Just click on the "Feedback" button in the top right to tell us what you think.
    </p>
</div>

### How do I use GitKraken Insights?

Insights can be accessed from [gitkraken.dev/insights](https://gitkraken.dev/insights).

In order to work with Insights, you will need to:
* [Connect an integration](/gk-dev/gk-dev-integrations/) from [gitkraken.dev/settings/integrations](https://gitkraken.dev/settings/integrations)
* And create a [Cloud Workspace](/gk-dev/gk-dev-home/#workspaces) from [gitkraken.dev/workspaces](https://gitkraken.dev/workspaces)

Once you have done both, you will be able to filter by a workspace to see the Insights for the repositories in that workspace. You can also filter by date range.

<img src="/wp-content/uploads/gkdev-insights-filters.png" srcset="/wp-content/uploads/gkdev-insights-filters@2x.png" class="img-bordered img-responsive center">

<div class='callout callout--note'>
    <p>
        Filtering by 14 days is available for Teams subscriptions and filtering by 28 days is available for Enterprise Subscriptions. 
    </p>
</div>

<div class='callout callout--note'>
    <p>
        <strong>Note:</strong> When using Insights, we will attempt to add webhooks to your workspace repositories in order to reduce API calls and improve data performance.
    </p>
</div>

### Metrics

Insights offer the following metrics. You can also hover over the <i class="fa-solid fa-circle-info"></i> icon to see a description of the metric.

* **Cycle Time**: Measures the average time it takes for a pull request to be merged for the selected timeframe.
* **Average Throughput**: Measures the average number of pull requests merged for the selected timeframe. 
* **Merge** Rate: The percentage of merged pull requests compared to open pull requests for the selected timeframe. 
* **Open**: The total number of pull requests opened for the selected timeframe.
* **Merged**: The total number of pull requests merged for the selected timeframe.

### Requirement for Azure Insights and Workspaces

In order to work with Insights and [Workspaces](/gitkraken-desktop/workspaces/) for Azure, `Third-party application access via OAuth` will need to be enabled in Azure from `Organization Settings > Policies`. You can find more information on this setting [here](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).