---
title: Dashboard Management in GitKraken Insights
description: Learn how to add and interpret key DORA and Pull Request metrics, arrange your layout, and use filters to analyze data on dashboards.
taxonomy:
    category: gk-dev
---
<kbd>Last updated: October 2025</kbd>


## Overview

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
  <img src="/wp-content/uploads/Insights-Dashboard.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Access your Insights Dashboard from gitkraken.dev.</figcaption>
</figure>

### Add a metric

1. In the Dashboard view, click the **Add Metric** button in the top-right corner.
2. Browse the list of available widgets, grouped by category (for example, **DORA** and **Pull Requests**).
3. Click **Add** next to the metric you want to display on your dashboard.

<figure>
  <img src="/wp-content/uploads/add-metric.png" srcset="/wp-content/uploads/add-metric@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Add DORA or PR metrics to your dashboard.</figcaption>
</figure>

### Available metrics

**DORA metrics**

- Deploy Frequency
- Change lead time
- Mean time to repair/recover
- Defect rate (% of deploy with severe defect)

**Pull Request metrics**

- First response time ("Pickup time")
- Cycle time ("first commit" to "merge")
- Lead time ("first commit" to "deployed")
- Number of reviews per day/week/month

### Deploy Frequency

This metric shows how often new code is released or deployed to production, measured as the number of deployments per day, week, or other selected timeframe.

<figure>
  <img src="/wp-content/uploads/deploy-frequency.png" srcset="/wp-content/uploads/deploy-frequency@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Shows deployments per day, week or selected timeframe.</figcaption>
</figure>

In addition to the main chart, the following submetrics are displayed when you click the Details button:

- **Deployments per day**
- **Lead time for changes**
- **Average hours to repair (MTTR)**
- **Change failure rate**

<figure>
  <img src="/wp-content/uploads/deployment-frequency-oct-2025.png" srcset="/wp-content/uploads/deployment-frequency-oct-2025@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Click the Details button to get 4 additional metrics.</figcaption>
</figure>

### Change Lead Time
This metric shows how long each pull request within a selected timeframe took to go from the first commit until it was deployed. Values are expressed in **days** and are calculated over a rolling **7-day period**.

<figure>
  <img src="/wp-content/uploads/change-lead-time.png" srcset="/wp-content/uploads/change-lead-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Shows how long each PR took from first commit to deployment.</figcaption>
</figure>

### Mean Time to Repair/Recover (MTTR)

This metric shows how long each pull request within a selected timeframe took to go from the first commit until it was deployed. Values are expressed in **days** and calculated over a rolling **7-day period**. Lower MTTR indicates that teams can respond quickly to incidents and minimize downtime.

### Defect Rate

This metric shows the number of defects detected over time. Values are expressed as **defects** over a rolling **7-day window**. A lower defect rate indicates a more stable and reliable deployment process.

### First Response Time ("Pickup Time")

This metric shows how long each pull request within a selected timeframe took to have a first response (comment or review). Values are expressed in **hours** and averaged over a **7-day period**. Shorter pickup times indicate faster reviewer engagement and healthier collaboration.

<figure>
  <img src="/wp-content/uploads/first-response-time.png" srcset="/wp-content/uploads/first-response-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Average time it took for PR to receive comment or review.</figcaption>
</figure>

### Cycle Time ("first commit" to "merge")

This metric shows how long each pull request within a selected timeframe took to merge from the time the first commit was made. Values are expressed in **days** and averaged over a **7-day period**. Cycle time provides insight into overall delivery speed, highlighting how quickly work moves from coding to production.

<figure>
  <img src="/wp-content/uploads/cycle-time-line.png" srcset="/wp-content/uploads/cycle-time-line@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Average time it took for PR to receive comment or review.</figcaption>
</figure>

The **Details** view offers deeper analysis.

<figure>
  <img src="/wp-content/uploads/pr-cycle-time-details.png" srcset="/wp-content/uploads/pr-cycle-time-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Get a detailed breakdown of PR cycle time.</figcaption>
</figure>

- Pull requests are grouped into four categories by duration:
  - **Elite:** Less than 1 day
  - **Fast:** 1–7 days
  - **Average:** 7–29 days
  - **Slower:** Over 30 days
- Each node in the scatter plot is interactive, showing PR details such as time since merge, PR name, author, and a link to open directly in GitHub.
- A sortable table lists all PRs below the chart. You can sort by **Days**, **Pull Request name**, **Author**, **Date Opened**, or **Date Merged**.

### Lead Time

This metric shows how long each pull request within a selected timeframe remained open, measured from when the PR was created until it was merged. Values are expressed in **days** and averaged over a **7-day period**.

<figure>
  <img src="/wp-content/uploads/lead-time.png" srcset="/wp-content/uploads/lead-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">See how long PRs remained open until it was merged.</figcaption>
</figure>

### Number of Reviews per Day/Week/Month

This metric shows the total number of reviews (all types) completed over a given period of time. Values are expressed in **reviews** and averaged over a **7-day window**. Tracking review activity helps teams understand collaboration patterns and reviewer workload across different timeframes (daily, weekly, or monthly).

<figure>
  <img src="/wp-content/uploads/number-of-reviews.png" srcset="/wp-content/uploads/number-of-reviews@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">See how many reviews have been given over a time period.</figcaption>
</figure>

---

## Layout

Widgets on the dashboard can be customized to fit your needs.

- **Resize widgets:** Each widget is available in two sizes—small or large. Drag and drop the lower-right corner of a widget to adjust its size.
- **Rearrange widgets:** Drag and drop from the upper-left corner of a widget to move it into a new position on the dashboard.
- **One per dashboard:** Only one copy of each metric can be placed on a dashboard.
- **Widget menu:** From the menu in the upper-right of each widget, you can switch between **line** and **bar** graph types, resize the widget between large or small, export the graph data, or remove the widget from the dashboard.

<figure>
  <img src="/wp-content/uploads/layout-options.png" srcset="/wp-content/uploads/layout-options@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Switch between bar or line graphs, resize, export graph data, or remove widget from the menu in the upper right.</figcaption>
</figure>

> **Note:** Currently, each user can create only one dashboard per organization. Support for multiple dashboards per user is planned for a future release.

---

## Filters

The dashboard may be filtered by **Workspace**, **Repositories**, **Timeframe**, and **Team**.

- **Workspace:** Workspaces are preset groups of repositories. They also enable other key features across gitkraken.dev, GitKraken Desktop, GitLens, and the GitKraken CLI such as Launchpad and multi-repo actions. On the dashboard, you can filter to only display data for the repositories in your chosen Workspace. To create your first workspace, go to [gitkraken.dev/workspaces](https://gitkraken.dev/workspaces).

- **Repositories:** Refers to the list of repos imported into GitKraken Insights. Check or uncheck repositories to fine-tune the data. Use the search feature to quickly locate repos by name.

- **Timeframe:** Sets the timebox for the dashboard. Options include **This Week, Last Week, Last 7 days, Last 14 days, Last 28 days, Last 30 days, Last 90 days, Last 12 months**, or a custom date range.

- **Team:** Filters the data by a group of users. To configure teams, go to **Insights > Settings > Setup your Team**.


<figure>
  <img src="/wp-content/uploads/timeframe-filter.png" srcset="/wp-content/uploads/timeframe-filter@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Filter your dashboard by Workspace, Repo, Timeframe, or Team.</figcaption>
</figure>