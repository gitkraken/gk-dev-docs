---
title: Dashboard Management in GitKraken Insights
description: Learn how to add and interpret key DORA and Pull Request metrics, arrange your layout, and use filters to analyze data on dashboards.
product: "GitKraken Insights"
content_type: "reference"
audience: "admin"
plan_required: [insights-add-on]
status: "preview"
last_verified: "2026-03"
feature: "Insights Dashboards"
git_hosts: [github]
integrations: []
hosted_variant: cloud
role_required: [Owner, Admin, Lead]
llms_include: true
tags: [insights, dashboards, metrics, dora, pull-requests, ai-impact, trendlines, filters]
taxonomy:
    category: gk-dev
custom_fields:
    nav_category: "gk-dev-insights"
    nav_label: "Dashboard Management in GitKraken Insights"
    nav_order: 10
    nav_parent: "gk-dev-insights"
    page_type: "content"
    anchor_map: ["deploy-frequency|/gk-insights/gk-insights-dora-metrics/#deploy-frequency", "change-lead-time|/gk-insights/gk-insights-dora-metrics/#change-lead-time", "mean-time-to-repairrecover-mttr|/gk-insights/gk-insights-dora-metrics/#mean-time-to-repairrecover-mttr", "defect-rate|/gk-insights/gk-insights-dora-metrics/#defect-rate", "first-response-time-pickup-time|/gk-insights/gk-insights-pr-metrics/#first-response-time-pickup-time", "cycle-time-first-commit-to-merge|/gk-insights/gk-insights-pr-metrics/#cycle-time-first-commit-to-merge", "lead-time|/gk-insights/gk-insights-pr-metrics/#lead-time", "number-of-reviews-per-dayweekmonth|/gk-insights/gk-insights-pr-metrics/#number-of-reviews-per-dayweekmonth", "open-time-opened-to-merged|/gk-insights/gk-insights-pr-metrics/#open-time-opened-to-merged", "number-of-prs-abandoned|/gk-insights/gk-insights-pr-metrics/#number-of-prs-abandoned", "number-of-prs-merged-without-review|/gk-insights/gk-insights-pr-metrics/#number-of-prs-merged-without-review", "number-of-pr-comments|/gk-insights/gk-insights-pr-metrics/#number-of-pr-comments", "pr-size--effort|/gk-insights/gk-insights-pr-metrics/#pr-size--effort", "code-review-hours|/gk-insights/gk-insights-pr-metrics/#code-review-hours", "copypaste-vs-moved-percent|/gk-insights/gk-insights-ai-impact-metrics/#copypaste-vs-moved-percent", "duplicated-code|/gk-insights/gk-insights-ai-impact-metrics/#duplicated-code", "percent-of-code-rework-churned-lines|/gk-insights/gk-insights-ai-impact-metrics/#percent-of-code-rework-churned-lines", "post-pr-work-occurring|/gk-insights/gk-insights-ai-impact-metrics/#post-pr-work-occurring", "active-users|/gk-insights/gk-insights-ai-impact-metrics/#active-users", "suggestions-by-total-lines|/gk-insights/gk-insights-ai-impact-metrics/#suggestions-by-total-lines", "prompt-acceptance-rate|/gk-insights/gk-insights-ai-impact-metrics/#prompt-acceptance-rate", "tab-acceptance-rate|/gk-insights/gk-insights-ai-impact-metrics/#tab-acceptance-rate", "bug-work-percent|/gk-insights/gk-insights-code-quality-metrics/#bug-work-percent", "documentation-and-test-percent|/gk-insights/gk-insights-code-quality-metrics/#documentation-and-test-percent", "code-change-rate|/gk-insights/gk-insights-code-quality-metrics/#code-change-rate", "code-change-by-operation|/gk-insights/gk-insights-code-quality-metrics/#code-change-by-operation", "commit-count|/gk-insights/gk-insights-velocity-metrics/#commit-count", "estimated-coding-hours|/gk-insights/gk-insights-velocity-metrics/#estimated-coding-hours"]
---
<kbd>Last updated: March 2026</kbd>

GitKraken Insights dashboards display engineering metrics from connected repositories, pull requests, CI/CD pipelines, and AI coding tools. Dashboards require completing Insights onboarding and importing at least one repository. GitKraken Insights is available as an add-on to GitKraken subscriptions or as a standalone product by request.

***

## Quick Start

Dashboards support filtering by Workspace, repository, timeframe, and team.

To add metrics to a dashboard:

1. Complete Insights onboarding by connecting a data source and importing repositories. See the [Getting Started guide](https://help.gitkraken.com/gk-dev/gk-dev-insights/).
2. Open [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken_dot_dev) and navigate to **Insights > Dashboard**.
3. Click **Add Metric** in the top-right corner.
4. Browse metric categories: DORA, Pull Requests, AI Impact, Code Quality, or Velocity/Delivery Consistency.
5. Click **Add** next to the desired metric to place it on the dashboard.
6. Resize widgets by dragging the lower-right corner. Reorder them by dragging the upper-left handle.

To create a separate view scoped to a team or project, select **+ Create dashboard** from the dropdown in the top-left corner. Each dashboard supports one copy of each metric.

***

## What GitKraken Insights dashboards show

GitKraken Insights brings your Git data, pull requests, issues, and CI/CD results into one place. Instead of juggling tools or exporting spreadsheets, you get dashboards that show how work is really moving across code, reviews, and releases. The goal is to give both devs and leads a clear view of progress and bottlenecks without extra reporting overhead.

### Key benefits

- **In your workflow:** Metrics come straight from the tools you already use: Git, PRs, CI/CD, issue trackers. No duplicate work, no disruption.  
- **Useful context:** See how code changes connect to tickets, review quality, and team goals. Less vanity stats, more signal.  
- **Clear next steps:** Spot inefficiencies and get practical ways to improve, whether it’s review speed, investment in features vs. fixes, or build times.  

---

## Adding Metrics

Before you can add metrics, complete these setup steps:

1. [Request a guided tour to get access](https://www.gitkraken.com/insights#form).
2. Connect GitKraken Insights to your GitHub account.
3. Wait for your repositories to finish importing. For detailed instructions, see the [Getting Started guide](https://help.gitkraken.com/gk-dev/gk-dev-insights).

Once setup is complete, open the **Insights > Dashboard** tab from [gitkraken.dev](https://gitkraken.dev).

<figure>
  <img src="/wp-content/uploads/Insights-Dashboard.png" class="help-center-img img-bordered" alt="GitKraken.dev interface showing how to access the Insights Dashboard with navigation menu highlighted and sample deployment metric displayed." />
  <figcaption style="text-align: center; color: #888">Access your Insights Dashboard from gitkraken.dev.</figcaption>
</figure>

### Creating Dashboards

You can create multiple dashboards in GitKraken Insights to organize metrics by team, project, or focus area. To begin, use the dropdown menu in the top-left corner of the dashboard view. From there, select **+ Create dashboard** to open the creation modal.

<figure>
  <img src="/wp-content/uploads/create-dashboard-dropdown.png" srcset="/wp-content/uploads/create-dashboard-dropdown@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights UI showing the GitLens Team dashboard dropdown with the Create dashboard option highlighted and a pointer hovering over it." />
  <figcaption style="text-align: center; color: #888">Use the dropdown menu to select an existing dashboard or create a new one.</figcaption>
</figure>

In the modal, enter a **Title** and optional **Description** to help distinguish this dashboard from others. Creating focused dashboards is especially helpful for tracking metrics by repository group, product area, or individual contributor activity.

<figure>
  <img src="/wp-content/uploads/create-dashboard-modal.png" srcset="/wp-content/uploads/create-dashboard-modal@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights modal for creating a new dashboard, showing fields for title and description, and a Create dashboard button." />
  <figcaption style="text-align: center; color: #888">Name your dashboard and optionally add a description to clarify its focus.</figcaption>
</figure>



### Add a metric

1. In the Dashboard view, click the **Add Metric** button in the top-right corner.
2. Browse the list of available widgets, grouped by category (for example, **DORA** and **Pull Requests**).
3. Click **Add** next to the metric you want to display on your dashboard.

<figure>
  <img src="/wp-content/uploads/add-metric.png" srcset="/wp-content/uploads/add-metric@2x.png" class="help-center-img img-bordered" alt="Dropdown menu in GitKraken Insights showing options to add DORA and pull request metrics to a dashboard" />
  <figcaption style="text-align: center; color: #888">Add DORA or PR metrics to your dashboard.</figcaption>
</figure>

### Available metrics

| Metric | Category | Unit | Use when you need to... |
|---|---|---|---|
| [Deploy Frequency](/gk-insights/gk-insights-dora-metrics/#deploy-frequency) | DORA | Deployments per period | Measure how often code reaches production |
| [Change Lead Time](/gk-insights/gk-insights-dora-metrics/#change-lead-time) | DORA | Days | Track time from first commit to deployment |
| [Mean Time to Repair](/gk-insights/gk-insights-dora-metrics/#mean-time-to-repairrecover-mttr) | DORA | Hours | Measure incident response and recovery speed |
| [Defect Rate](/gk-insights/gk-insights-dora-metrics/#defect-rate) | DORA | Percentage | Assess deployment stability and failure rate |
| [First Response Time](/gk-insights/gk-insights-pr-metrics/#first-response-time-pickup-time) | Pull Requests | Hours | Identify delays in initial PR review engagement |
| [Cycle Time](/gk-insights/gk-insights-pr-metrics/#cycle-time-first-commit-to-merge) | Pull Requests | Days | Measure total time from first commit to merge |
| [Lead Time](/gk-insights/gk-insights-pr-metrics/#lead-time) | Pull Requests | Days | Measure total time from first commit to deployment |
| [Number of Reviews](/gk-insights/gk-insights-pr-metrics/#number-of-reviews-per-dayweekmonth) | Pull Requests | Count per period | Track review activity and reviewer workload |
| [Open Time](/gk-insights/gk-insights-pr-metrics/#open-time-opened-to-merged) | Pull Requests | Days | Isolate the review and approval phase duration |
| [PRs Abandoned](/gk-insights/gk-insights-pr-metrics/#number-of-prs-abandoned) | Pull Requests | Count | Detect wasted effort or scope management issues |
| [PRs Merged Without Review](/gk-insights/gk-insights-pr-metrics/#number-of-prs-merged-without-review) | Pull Requests | Count | Identify gaps in code review enforcement |
| [PR Comments](/gk-insights/gk-insights-pr-metrics/#number-of-pr-comments) | Pull Requests | Count | Gauge review depth and collaboration intensity |
| [PR Size/Effort](/gk-insights/gk-insights-pr-metrics/#pr-size--effort) | Pull Requests | Lines changed | Evaluate review load and identify oversized PRs |
| [Code Review Hours](/gk-insights/gk-insights-pr-metrics/#code-review-hours) | Pull Requests | Hours | Assess team investment in code review |
| [Copy/Paste vs Moved](/gk-insights/gk-insights-ai-impact-metrics/#copypaste-vs-moved-percent) | AI Impact | Percentage | Distinguish duplication from healthy refactoring |
| [Duplicated Code](/gk-insights/gk-insights-ai-impact-metrics/#duplicated-code) | AI Impact | Lines | Track redundant code blocks across repos |
| [Code Rework](/gk-insights/gk-insights-ai-impact-metrics/#percent-of-code-rework-churned-lines) | AI Impact | Percentage | Identify instability or premature code changes |
| [Post PR Work](/gk-insights/gk-insights-ai-impact-metrics/#post-pr-work-occurring) | AI Impact | Lines | Measure rework needed after merging |
| [Active Users](/gk-insights/gk-insights-ai-impact-metrics/#active-users) | AI Impact | Count | Track AI coding tool adoption across teams |
| [Suggestions](/gk-insights/gk-insights-ai-impact-metrics/#suggestions-by-total-lines) | AI Impact | Lines | Measure volume of AI-generated code suggestions |
| [Prompt Acceptance Rate](/gk-insights/gk-insights-ai-impact-metrics/#prompt-acceptance-rate) | AI Impact | Percentage | Gauge developer trust in AI suggestions |
| [Tab Acceptance Rate](/gk-insights/gk-insights-ai-impact-metrics/#tab-acceptance-rate) | AI Impact | Percentage | Measure frictionless AI suggestion adoption |
| [Bug Work Percent](/gk-insights/gk-insights-code-quality-metrics/#bug-work-percent) | Code Quality | Percentage | Assess proportion of effort spent on bug fixes |
| [Documentation and Test %](/gk-insights/gk-insights-code-quality-metrics/#documentation-and-test-percent) | Code Quality | Percentage | Monitor investment in tests and documentation |
| [Code Change Rate](/gk-insights/gk-insights-code-quality-metrics/#code-change-rate) | Code Quality | Lines by age | Identify technical debt hotspots in older code |
| [Code Change by Operation](/gk-insights/gk-insights-code-quality-metrics/#code-change-by-operation) | Code Quality | Lines by type | Visualize effort distribution across system layers |
| [Commit Count](/gk-insights/gk-insights-velocity-metrics/#commit-count) | Velocity | Count | Track development activity volume |
| [Estimated Coding Hours](/gk-insights/gk-insights-velocity-metrics/#estimated-coding-hours) | Velocity | Hours | Approximate total active development time |

> **Use Cycle Time** to measure from first commit to merge (development speed). **Use Open Time** to isolate just the review phase (review efficiency). **Use Lead Time** to measure from first commit to deployment (end-to-end delivery).


***

## DORA metrics

DORA (DevOps Research and Assessment) metrics are a standardized set of four key performance indicators: deployment frequency, lead time for changes, change failure rate, and time to restore service. 

Developed by a Google Cloud research team, these metrics help organizations measure DevOps performance, identify areas for improvement, and deliver software more efficiently and reliably.

For the definition of each metric, see [DORA Metrics in GitKraken Insights](/gk-insights/gk-insights-dora-metrics/).

***

## Pull Request metrics

Pull Request metrics help teams understand how quickly and smoothly code changes move through review and deployment. 

PR intelligence turns these insights into clear actions by highlighting slowdowns, spotting patterns in fast or delayed reviews, and uncovering blockers that may affect delivery.

For the definition of each metric, see [Pull Request Metrics in GitKraken Insights](/gk-insights/gk-insights-pr-metrics/).

***

## AI Impact

AI Impact metrics help teams understand how AI coding tools affect code quality and developer efficiency. By tracking rework, duplication, and post-PR changes, teams can see measurable improvements in code and workflow, proving ROI and guiding smarter use of AI tools.

For the definition of each metric, see [AI Impact Metrics in GitKraken Insights](/gk-insights/gk-insights-ai-impact-metrics/).

---

## Code Quality

This section presents metrics designed to assess and improve engineering quality. Together, they offer a balanced view of code health by examining how much work is spent on bugs, tests, and documentation, how frequently older code is modified, and how engineering effort is distributed across different parts of the system.

Use these metrics to monitor technical debt, maintain development quality, and align team investments with maintainability and product stability goals.

For the definition of each metric, see [Code Quality Metrics in GitKraken Insights](/gk-insights/gk-insights-code-quality-metrics/).

***

## Velocity/Delivery Consistency

This section highlights metrics that reflect development rhythm and consistency. Tracking commit volume and coding hours helps teams assess delivery patterns and ensure developers have time for focused work.

For the definition of each metric, see [Velocity and Delivery Consistency Metrics in GitKraken Insights](/gk-insights/gk-insights-velocity-metrics/).

***
## How to customize dashboard layout

Widgets on the dashboard can be customized to fit your needs.

- **Resize widgets:** Each widget is available in two sizes—small or large. Drag and drop the lower-right corner of a widget to adjust its size.
- **Rearrange widgets:** Drag and drop from the upper-left corner of a widget to move it into a new position on the dashboard.
- **One per dashboard:** Only one copy of each metric can be placed on a dashboard.
- **Widget menu:** From the menu in the upper-right of each widget, you can switch between **line** and **bar** graph types, resize the widget between large or small, export the graph data, or remove the widget from the dashboard.
- **Switch graph type** Switch between line graphs, area graphs, or bar graphs.

<figure>
  <img src="/wp-content/uploads/layout-options.png" srcset="/wp-content/uploads/layout-options@2x.png" class="help-center-img img-bordered" alt="Cycle time line graph with dropdown menu expanded showing options such as switching to bar graph, resizing, exporting data, or removing the widget" />
  <figcaption style="text-align: center; color: #888">Switch between bar, area or line graphs, resize, export graph data, or remove widget from the menu in the upper right.</figcaption>
</figure>

> **Note:** Currently, each user can create only one dashboard per organization. Support for multiple dashboards per user is planned for a future release.

---

## How to add trendlines to charts

You can add trendlines to any chart in GitKraken Insights to help visualize patterns over time. These overlays make it easier to understand whether your metrics are improving, declining, or fluctuating—and how consistently.

### How to add a trendline

1. On any dashboard widget, click the **⋯ (three dots)** menu in the upper-right corner.
2. Select **Set trendline**.
3. Choose one of the available types:

- **None:** No trendline is shown.
- **Linear:** Adds a straight line through the data to show steady upward or downward trends.
- **Polynomial:** Adds a curved line that reveals acceleration, deceleration, or changing directions in the data.
- **Moving Average:** Smooths out short-term fluctuations to highlight the overall pattern, especially useful for noisy or jumpy data.

<figure>
  <img src="/wp-content/uploads/trendline-menu.png" srcset="/wp-content/uploads/trendline-menu@2x.png" class="help-center-img img-bordered" alt="Mean Time to Repair chart with menu open showing trendline options including None, Polynomial, and Moving Average" />
  <figcaption style="text-align: center; color: #888">From the widget menu, select a trendline type to better understand long-term changes in your metrics.</figcaption>
</figure>

> **Tip:** Use trendlines to spot steady improvements, regressions, or shifts in behavior across delivery, review, or quality metrics.

***

## How to filter dashboard data

The dashboard may be filtered by **Workspace**, **Repositories**, **Timeframe**, and **Team**.

- **Workspace:** Workspaces are preset groups of repositories. They also enable other key features across gitkraken.dev, GitKraken Desktop, GitLens, and the GitKraken CLI such as Launchpad and multi-repo actions. On the dashboard, you can filter to only display data for the repositories in your chosen Workspace. To create your first workspace, go to [gitkraken.dev/workspaces](https://gitkraken.dev/workspaces).

- **Repositories:** Refers to the list of repos imported into GitKraken Insights. Check or uncheck repositories to fine-tune the data. Use the search feature to quickly locate repos by name.

- **Timeframe:** Sets the timebox for the dashboard. Options include **This Week, Last Week, Last 7 days, Last 14 days, Last 28 days, Last 30 days, Last 90 days, Last 12 months**, or a custom date range.

- **Team:** Filters the data by a group of users. To configure teams, go to **Insights > Settings > Setup your Team**.


<figure>
  <img src="/wp-content/uploads/timeframe-filter.png" srcset="/wp-content/uploads/timeframe-filter@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights dashboard with filters for Workspace, Repository, Team, and Timeframe shown with a 90-day range selected in the calendar" />
  <figcaption style="text-align: center; color: #888">Filter your dashboard by Workspace, Repo, Timeframe, or Team.</figcaption>
</figure>