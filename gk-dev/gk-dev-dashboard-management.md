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

## Available metrics

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

**AI Impact metrics**

- Copy/paste vs moved percent
- Duplicated code
- Percent of code rework (churned lines)
- Post PR work occurring


## DORA metrics

DORA (DevOps Research and Assessment) metrics are a standardized set of four key performance indicators: deployment frequency, lead time for changes, change failure rate, and time to restore service. 

Developed by a Google Cloud research team, these metrics help organizations measure DevOps performance, identify areas for improvement, and deliver software more efficiently and reliably.

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

## Pull Request metrics

Pull Request metrics help teams understand how quickly and smoothly code changes move through review and deployment. 

PR intelligence turns these insights into clear actions by highlighting slowdowns, spotting patterns in fast or delayed reviews, and uncovering blockers that may affect delivery.

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

## AI Impact

AI Impact metrics help teams understand how AI coding tools affect code quality and developer efficiency. By tracking rework, duplication, and post-PR changes, teams can see measurable improvements in code and workflow, proving ROI and guiding smarter use of AI tools.

### Copy/paste vs moved percent

The Copy/Paste vs Moved Percent metric compares how much code is duplicated versus refactored or relocated over time. When the copy/paste percentage is higher than the moved percentage, it suggests that developers are duplicating code instead of reusing or restructuring it, which can lead to higher maintenance costs and lower overall code quality. 

<figure>
  <img src="/wp-content/uploads/copy-paste-moved.png" srcset="/wp-content/uploads/copy-paste-moved@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Compare duplicated versus refactored code over time to identify reuse and duplication trends.</figcaption>
</figure>

You can hover over points on the chart to view the exact percentages for a specific time period, making it easy to see changes before and after implementing an AI coding tool.


### Duplicated code

The Duplicated Code metric highlights how much code is being repeated across your repositories, helping teams identify inefficiencies and potential maintainability issues. When duplication rises, it often signals that AI-assisted or manual coding practices are reusing code without enough refactoring. 

<figure>
  <img src="/wp-content/uploads/duplicated-code.png" srcset="/wp-content/uploads/duplicated-code@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how duplicated code changes over time to identify growth in repeated code patterns.</figcaption>
</figure>

The detailed view breaks this down by repository and time period, showing where duplication is concentrated and how it changes alongside overall development activity, such as commits, pull requests, and issues resolved. This helps teams connect code duplication trends to broader workflow patterns and assess the real impact of AI tools on code quality.

<figure>
  <img src="/wp-content/uploads/duplicated-code-details.png" srcset="/wp-content/uploads/duplicated-code-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View duplicated code by repository to see which projects contribute most to redundancy.</figcaption>
</figure>

### Percent of code rework (churned lines)

The Percent of Code Rework (Churned Lines) metric measures how often recently written code is rewritten, deleted, or replaced over time. High churn rates can indicate instability, unclear requirements, or inefficiencies in AI-assisted code generation. 

<figure>
  <img src="/wp-content/uploads/percent-of-code-rework.png" srcset="/wp-content/uploads/percent-of-code-rework@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how frequently code is rewritten or replaced over time to identify rework trends.</figcaption>
</figure>

The detailed view breaks this down across repositories and time periods, helping teams see where rework is concentrated and how it aligns with activity levels like commits, pull requests, and issue resolutions. By monitoring this metric, teams can assess whether AI tools are improving long-term code quality or introducing avoidable rework.

<figure>
  <img src="/wp-content/uploads/duplicated-code-details-view.png" srcset="/wp-content/uploads/duplicated-code-details-view@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View rework percentages by repository to pinpoint where churn is most frequent.</figcaption>
</figure>

### Post PR work occurring

The Post PR Work Occurring metric measures how much additional code is written or modified after a pull request has been merged. This helps teams spot follow-up work that may indicate incomplete reviews, rushed merges, or overlooked issues during initial development. 

<figure>
  <img src="/wp-content/uploads/post-pr-work-occuring.png" srcset="/wp-content/uploads/post-pr-work-occuring@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how much post-merge work occurs over time to identify spikes in follow-up activity.</figcaption>
</figure>

The detailed view breaks this activity down by repository and time period, revealing patterns in post-merge changes and how they relate to broader development activity, such as commits and pull requests. Tracking this metric over time helps teams improve review quality and identify whether AI-assisted coding leads to more—or less—post-merge rework.

<figure>
  <img src="/wp-content/uploads/post-pr-work-occuring-details.png" srcset="/wp-content/uploads/post-pr-work-occuring-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View post-merge work by repository to see where additional changes are concentrated.</figcaption>
</figure>


---

## Layout

Widgets on the dashboard can be customized to fit your needs.

- **Resize widgets:** Each widget is available in two sizes—small or large. Drag and drop the lower-right corner of a widget to adjust its size.
- **Rearrange widgets:** Drag and drop from the upper-left corner of a widget to move it into a new position on the dashboard.
- **One per dashboard:** Only one copy of each metric can be placed on a dashboard.
- **Widget menu:** From the menu in the upper-right of each widget, you can switch between **line** and **bar** graph types, resize the widget between large or small, export the graph data, or remove the widget from the dashboard.
- **Switch graph type** Switch between line graphs, area graphs, or bar graphs.

<figure>
  <img src="/wp-content/uploads/layout-options.png" srcset="/wp-content/uploads/layout-options@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Switch between bar, area or line graphs, resize, export graph data, or remove widget from the menu in the upper right.</figcaption>
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