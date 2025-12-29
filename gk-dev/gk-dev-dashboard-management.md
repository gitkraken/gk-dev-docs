---
title: Dashboard Management in GitKraken Insights
description: Learn how to add and interpret key DORA and Pull Request metrics, arrange your layout, and use filters to analyze data on dashboards.
taxonomy:
    category: gk-dev
---
<kbd>Last updated: December 2025</kbd>


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
- Open Time ("opened" to "merged")
- Number of PRs Abandoned
- Number of PRs Merged Without Review
- Number of PR Comments
- PR Size/Effort
- Code Review Hours

**AI Impact metrics**

- Copy/paste vs moved percent
- Duplicated code
- Percent of code rework (churned lines)
- Post PR work occurring
- Active Users
- Suggestions (by total lines)
- Prompt Acceptance Rate
- Tab Acceptance Rate

**Code Quality metrics**

- Bug Work Percent
- Documentation and Test Percent
- Code Change Rate
- Code Change by Operation

**Velocity/Delivery Consistency**

- Commit Count
- Estimated Coding Hours

### Creating Dashboards

You can create multiple dashboards in GitKraken Insights to organize metrics by team, project, or focus area. To begin, use the dropdown menu in the top-left corner of the dashboard view. From there, select **+ Create dashboard** to open the creation modal.

<figure>
  <img src="/wp-content/uploads/create-dashboard-dropdown.png" srcset="/wp-content/uploads/create-dashboard-dropdown@2x.png" class="help-center-img img-bordered" alt="Dashboard dropdown showing Create dashboard option" />
  <figcaption style="text-align: center; color: #888">Use the dropdown menu to select an existing dashboard or create a new one.</figcaption>
</figure>

In the modal, enter a **Title** and optional **Description** to help distinguish this dashboard from others.

<figure>
  <img src="/wp-content/uploads/create-dashboard-modal.png" srcset="/wp-content/uploads/create-dashboard-modal@2x.png" class="help-center-img img-bordered" alt="Create dashboard modal with title and description fields" />
  <figcaption style="text-align: center; color: #888">Name your dashboard and optionally add a description to clarify its focus.</figcaption>
</figure>

Creating focused dashboards is especially helpful for tracking metrics by repository group, product area, or individual contributor activity.


***

## DORA metrics

DORA (DevOps Research and Assessment) metrics are a standardized set of four key performance indicators: deployment frequency, lead time for changes, change failure rate, and time to restore service. 

Developed by a Google Cloud research team, these metrics help organizations measure DevOps performance, identify areas for improvement, and deliver software more efficiently and reliably.

### Deploy Frequency

**Definition:** _The total number of deployments, as determined by the rules configured in the **Releases** settings._

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

**Definition:** _The time between the first commit linked to an issue (such as a Jira ticket) and when the associated code is deployed._

This metric shows how long each pull request within a selected timeframe took to go from the first commit until it was deployed. Values are expressed in **days** and are calculated over a rolling **7-day period**.

<figure>
  <img src="/wp-content/uploads/change-lead-time.png" srcset="/wp-content/uploads/change-lead-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Shows how long each PR took from first commit to deployment.</figcaption>
</figure>

### Mean Time to Repair/Recover (MTTR)

**Definition:** _Business hours between "defect detected" and "final fix deployed"._

This metric shows how long each pull request within a selected timeframe took to go from the first commit until it was deployed. Values are expressed in **days** and calculated over a rolling **7-day period**. Lower MTTR indicates that teams can respond quickly to incidents and minimize downtime.

### Defect Rate

**Definition:** _The percentage of deployments that resolve a critical defect. This metric measures the stability and quality of your deployment process._

This metric shows the number of defects detected over time. Values are expressed as **defects** over a rolling **7-day window**. A lower defect rate indicates a more stable and reliable deployment process.

***

## Pull Request metrics

Pull Request metrics help teams understand how quickly and smoothly code changes move through review and deployment. 

PR intelligence turns these insights into clear actions by highlighting slowdowns, spotting patterns in fast or delayed reviews, and uncovering blockers that may affect delivery.

### First Response Time ("Pickup Time")

**Definition:** _The time measured from when a PR is opened to when the 1st review or comment is left on a PR._

This metric shows how long each pull request within a selected timeframe took to have a first response (comment or review). Values are expressed in **hours** and averaged over a **7-day period**. Shorter pickup times indicate faster reviewer engagement and healthier collaboration.

<figure>
  <img src="/wp-content/uploads/first-response-time.png" srcset="/wp-content/uploads/first-response-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Average time it took for PR to receive comment or review.</figcaption>
</figure>

### Cycle Time ("first commit" to "merge")

**Definition:** _The time measured between the 1st commit of a PR to when the PR is merged._

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

**Definition:** _The time from the first commit in a pull request to when that code is deployed to production. This bridges development and deployment activities._

This metric shows how long each pull request within a selected timeframe remained open, measured from when the PR was created until it was merged. Values are expressed in **days** and averaged over a **7-day period**.

<figure>
  <img src="/wp-content/uploads/lead-time.png" srcset="/wp-content/uploads/lead-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">See how long PRs remained open until it was merged.</figcaption>
</figure>

### Number of Reviews per Day/Week/Month

**Definition:** _The volume of code reviews being conducted, indicating team review capacity and activity._

This metric shows the total number of reviews (all types) completed over a given period of time. Values are expressed in **reviews** and averaged over a **7-day window**. Tracking review activity helps teams understand collaboration patterns and reviewer workload across different timeframes (daily, weekly, or monthly).

<figure>
  <img src="/wp-content/uploads/number-of-reviews.png" srcset="/wp-content/uploads/number-of-reviews@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">See how many reviews have been given over a time period.</figcaption>
</figure>

### Open Time ("opened" to "merged")

**Definition:** _The time between when a pull request is opened and when it is merged._

This metric captures the duration from pull request creation to merge. It differs from PR Cycle Time, which starts from the first commit. Open Time isolates the review and approval phase, helping teams identify delays specifically related to code review and collaboration workflows.

<figure>
  <img src="/wp-content/uploads/open-time.png" srcset="/wp-content/uploads/open-time@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Shows the time each pull request remained open before being merged.</figcaption>
</figure>

The **Open Time details view** provides a stacked bar chart that visualizes average PR open durations per repository across time intervals. Each bar segment represents a specific repository, allowing teams to compare performance across services.

<figure>
  <img src="/wp-content/uploads/open-time-details.png" srcset="/wp-content/uploads/open-time-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Detailed breakdown of PR open durations across repositories and time intervals.</figcaption>
</figure>

Key highlights include:

- **Hover insights**: Hovering over bars shows per-repository open time for the selected week.
- **Repository comparison**: See how review duration varies across services.
- **Summary metrics**:
  - Pull requests merged
  - Pull request cycle time
  - Pull request average diff delta
  - Pull requests opened

These metrics help teams identify trends, uncover review bottlenecks, and monitor efficiency over time.

### Number of PRs Abandoned

**Definition:** _Number of pull requests closed without being merged._

This metric can reveal wasted engineering effort, scope management issues, or breakdowns in work planning and prioritization. A high abandonment rate may indicate unclear requirements, excessive rework, or bottlenecks earlier in the development process.

<figure>
  <img src="/wp-content/uploads/prs-abandoned.png" srcset="/wp-content/uploads/prs-abandoned@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Visualizes how many PRs were closed without merging, segmented by repository and time.</figcaption>
</figure>

### Number of PRs Merged Without Review

**Definition:** _The number of pull requests that have been merged without any (bot or human) review._

This metric can indicate potential process gaps in peer review enforcement. It identifies PRs integrated without peer review, exposing quality risks and gaps in your code review governance that could lead to production defects.

<figure>
  <img src="/wp-content/uploads/prs-merged-without-review.png" srcset="/wp-content/uploads/prs-merged-without-review@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Tracks PRs merged without review, highlighting enforcement issues in your review process.</figcaption>
</figure>

### Number of PR Comments

**Definition:** _The total number of comments left on your pull requests._

This metric measures the level of engagement during code reviews, revealing how thoroughly code is being evaluated. A high number of comments can indicate active feedback, knowledge sharing, and mentorship opportunities across the team.

<figure>
  <img src="/wp-content/uploads/pr-comments.png" srcset="/wp-content/uploads/pr-comments@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Shows total PR comments, which can reflect review depth and collaboration intensity.</figcaption>
</figure>

### PR Size / Effort

**Definition:** The aggregate amount of change (diff delta) across all pull requests that were merged during a given time period.

This metric reflects the total effort involved in the review process. It is calculated by summing the "Before PR submitted" and "While under review" diff delta values, representing the total size of the pull request and the energy required for its review.

<figure>
  <img src="/wp-content/uploads/pr-size.png" srcset="/wp-content/uploads/pr-size@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Displays total PR size (diff delta), helping evaluate review load and PR size trends.</figcaption>
</figure>

By aggregatating the total change volume across merged PRs, this helps teams balance workload distribution and recognize when PRs may be too large for effective review.

### Code Review Hours

**Definition:** Average time spent in hours during the "review period" of your team's pull requests.

**How it's calculated:** Total review hours / number of committers.

This metric quantifies the average time investment in reviewing code. It helps leaders evaluate whether code review capacity aligns with delivery goals and whether review processes need optimization to support team velocity and quality.

<figure>
  <img src="/wp-content/uploads/code-review-hours.png" srcset="/wp-content/uploads/code-review-hours@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Average code review time per developer, highlighting team review investment trends.</figcaption>
</figure>


***

## AI Impact

AI Impact metrics help teams understand how AI coding tools affect code quality and developer efficiency. By tracking rework, duplication, and post-PR changes, teams can see measurable improvements in code and workflow, proving ROI and guiding smarter use of AI tools.

### Copy/Paste vs Moved Percent

**Definition:** _This metric compares how much code is duplicated versus refactored or relocated over time. Moved lines reflect healthy code reorganization, while copy/pasted lines often signal duplicated logic that can lead to technical debt._

Tracking this metric helps teams distinguish between maintainable refactoring and potentially problematic duplication. This is especially important for teams using AI coding assistants, which tend to duplicate code rather than abstract or reuse it—leading to higher long-term maintenance costs if left unchecked.

<figure>
  <img src="/wp-content/uploads/copy-paste-moved.png" srcset="/wp-content/uploads/copy-paste-moved@2x.png" class="help-center-img img-bordered" alt="Line chart comparing duplicated and moved code over time" />
  <figcaption style="text-align: center; color: #888">Compare duplicated versus refactored code over time to identify reuse and duplication trends.</figcaption>
</figure>

You can hover over points on the chart to view the exact percentages for a specific time period, making it easy to see changes before and after implementing an AI coding tool.


### Duplicated Code

**Definition:** _The amount of lines in duplicate blocks detected._

This metric measures redundant code blocks in your codebase. It correlates with increased maintenance costs and a higher risk of defect propagation, since duplicated logic must be updated consistently across multiple places.

When duplication rises, it often signals that AI-assisted or manual coding practices are reusing code without enough refactoring.

<figure>
  <img src="/wp-content/uploads/duplicated-code.png" srcset="/wp-content/uploads/duplicated-code@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how duplicated code changes over time to identify growth in repeated code patterns.</figcaption>
</figure>

The detailed view breaks this down by repository and time period, showing where duplication is concentrated and how it changes alongside overall development activity, such as commits, pull requests, and issues resolved. This helps teams connect code duplication trends to broader workflow patterns and assess the real impact of AI tools on code quality.

<figure>
  <img src="/wp-content/uploads/duplicated-code-details.png" srcset="/wp-content/uploads/duplicated-code-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View duplicated code by repository to see which projects contribute most to redundancy.</figcaption>
</figure>

### Percent of Code Rework (Churned Lines)

**Definition:** _The percentage of recently written code that gets modified again quickly, which may indicate instability or changing requirements._

This metric calculates how much recently written code gets modified again, signaling instability, shifting requirements, or potential quality issues. High churn rates can reflect rework caused by unclear goals, rushed reviews, or limitations in AI-assisted code generation.

<figure>
  <img src="/wp-content/uploads/percent-of-code-rework.png" srcset="/wp-content/uploads/percent-of-code-rework@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how frequently code is rewritten or replaced over time to identify rework trends.</figcaption>
</figure>

The detailed view breaks this down across repositories and time periods, helping teams see where rework is concentrated and how it aligns with activity levels like commits, pull requests, and issue resolutions. By monitoring this metric, teams can assess whether AI tools are improving long-term code quality or introducing avoidable rework.

<figure>
  <img src="/wp-content/uploads/duplicated-code-details-view.png" srcset="/wp-content/uploads/duplicated-code-details-view@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View rework percentages by repository to pinpoint where churn is most frequent.</figcaption>
</figure>

### Post PR Work Occurring

**Definition:** _Follow-up work and bug fixes needed after merging, indicating the initial quality of AI-assisted code._

This metric quantifies rework and fixes needed after a pull request is merged, providing an early signal of code quality. It is especially useful when evaluating AI-assisted development, where code may pass initial review but still require corrections post-merge.

<figure>
  <img src="/wp-content/uploads/post-pr-work-occuring.png" srcset="/wp-content/uploads/post-pr-work-occuring@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how much post-merge work occurs over time to identify spikes in follow-up activity.</figcaption>
</figure>

The detailed view breaks this activity down by repository and time period, revealing patterns in post-merge changes and how they relate to broader development activity, such as commits and pull requests. Tracking this metric over time helps teams improve review quality and identify whether AI-assisted coding leads to more—or less—post-merge rework.

<figure>
  <img src="/wp-content/uploads/post-pr-work-occuring-details.png" srcset="/wp-content/uploads/post-pr-work-occuring-details@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">View post-merge work by repository to see where additional changes are concentrated.</figcaption>
</figure>

### Active Users

**Definition:** _The total count of unique users active in the connected AI provider integrations._

This metric counts developers actively using AI coding assistants from connected providers. It establishes a baseline for tracking AI adoption across your teams and supports analysis of AI tool investment impact and developer productivity trends.

<figure>
  <img src="/wp-content/uploads/active-users.png" srcset="/wp-content/uploads/active-users@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">See how many developers are actively using AI coding tools over time.</figcaption>
</figure>

### Suggestions (by total lines)

**Definition:** _The number of suggestions offered from your connected AI provider integrations._

This metric tracks the volume of AI-generated code suggestions offered to developers. It provides scale context for measuring the extent of AI contribution to overall development output and helps teams evaluate how heavily AI is being leveraged in the coding process.

<figure>
  <img src="/wp-content/uploads/suggestions.png" srcset="/wp-content/uploads/suggestions@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track the number of AI-generated suggestions to understand their influence on development activity.</figcaption>
</figure>

### Prompt Acceptance Rate

**Definition:** _The percentage of prompt results a developer accepted from your connected AI provider integrations._

This metric measures how many AI-generated code suggestions are accepted by developers. A higher rate indicates stronger alignment between AI outputs and developer expectations, signaling trust and effectiveness in AI-assisted workflows.


<figure>
  <img src="/wp-content/uploads/prompt-acceptance.png" srcset="/wp-content/uploads/prompt-acceptance@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Visualize how often AI suggestions are accepted by developers over time.</figcaption>
</figure>

### Tab Acceptance Rate

**Definition:** _Measures what percentage of AI-generated code suggestions developers accept with tabs._

Like prompt acceptance, this metric reflects the effectiveness and usability of AI suggestions. A higher tab acceptance rate indicates that developers find the suggestions useful and frictionless to apply, helping gauge the seamlessness of AI integration in development workflows.


<figure>
  <img src="/wp-content/uploads/tab-acceptance.png" srcset="/wp-content/uploads/tab-acceptance@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Track how frequently AI suggestions are accepted via tab completion.</figcaption>
</figure>

---

## Code Quality

This section presents metrics designed to assess and improve engineering quality. Together, they offer a balanced view of code health by examining how much work is spent on bugs, tests, and documentation, how frequently older code is modified, and how engineering effort is distributed across different parts of the system.

Use these metrics to monitor technical debt, maintain development quality, and align team investments with maintainability and product stability goals.


### Bug Work Percent

**Definition:** _The ratio of development work spent on fixing bugs vs everything else._

This metric reveals the proportion of engineering work consumed by fixing defects versus feature development. It helps leaders assess the level of code quality debt and prioritize efforts toward refactoring and process improvements.

<figure>
  <img src="/wp-content/uploads/bug-work-percent.png" srcset="/wp-content/uploads/bug-work-percent@2x.png" class="help-center-img img-bordered" alt="Chart showing percentage of work on bug fixes over time" />
  <figcaption style="text-align: center; color: #888">See how much development effort is spent resolving bugs compared to building new features.</figcaption>
</figure>

### Documentation and Test Percent

**Definition:** _The percent of work related to tests and documentation._

This metric shows the proportion of engineering work dedicated to writing tests and documentation. These activities are strong indicators of long-term maintainability and help improve onboarding efficiency, especially in growing or distributed teams.

<figure>
  <img src="/wp-content/uploads/doc-test-percent.png" srcset="/wp-content/uploads/doc-test-percent@2x.png" class="help-center-img img-bordered" alt="Chart showing percentage of test and documentation work" />
  <figcaption style="text-align: center; color: #888">Track how much work goes into tests and documentation over time.</figcaption>
</figure>

### Code Change Rate

**Definition:** _How old the code is that is being changed._

This metric tracks the age of code being modified. Frequent changes to older code may reveal technical debt hotspots, signaling the need for deeper refactoring or even system replacement. Teams can use this data to prioritize stability improvements and architectural upgrades.

<figure>
  <img src="/wp-content/uploads/code-change-rate.png" srcset="/wp-content/uploads/code-change-rate@2x.png" class="help-center-img img-bordered" alt="Chart showing age of code being modified" />
  <figcaption style="text-align: center; color: #888">See how much work targets older code, highlighting potential legacy or debt-heavy areas.</figcaption>
</figure>

### Code Change by Operation

**Definition:** _The measure of code changes organized by the type of change. (e.g., "test," "documentation," "front-end," "back-end")_

This metric breaks down engineering work by category, such as testing, documentation, front-end, and back-end development. It helps teams visualize where their effort is being spent and supports more strategic allocation of resources across system layers and quality activities.

<figure>
  <img src="/wp-content/uploads/code-change-by-operation.png" srcset="/wp-content/uploads/code-change-by-operation@2x.png" class="help-center-img img-bordered" alt="Chart showing breakdown of code changes by category" />
  <figcaption style="text-align: center; color: #888">Understand the distribution of code changes across different areas of the codebase.</figcaption>
</figure>

***

## Velocity/Delivery Consistency

This section highlights metrics that reflect development rhythm and consistency. Tracking commit volume and coding hours helps teams assess delivery patterns and ensure developers have time for focused work.

### Commit Count

**Definition:** _The number of commits pushed to all connected repositories._

This metric tracks the volume of code commits over time, offering a basic signal of development activity. While not a productivity metric on its own, it can help identify engagement patterns, team rhythm, and delivery frequency.

<figure>
  <img src="/wp-content/uploads/commit-count.png" srcset="/wp-content/uploads/commit-count@2x.png" class="help-center-img img-bordered" alt="Chart showing total commit volume" />
  <figcaption style="text-align: center; color: #888">Track how often developers commit code across connected repositories.</figcaption>
</figure>

### Estimated Coding Hours

**Definition:** _Estimates the amount of time a team's developers spend coding._

This metric approximates the total active development time across your team. It helps leaders assess engineering capacity, detect shifts in focus time, and understand whether developers are able to engage in deep work versus being blocked or interrupted.

<figure>
  <img src="/wp-content/uploads/estimated-coding-hours.png" srcset="/wp-content/uploads/estimated-coding-hours@2x.png" class="help-center-img img-bordered" alt="Chart showing estimated time spent coding" />
  <figcaption style="text-align: center; color: #888">Visualize how much time teams spend actively coding over time.</figcaption>
</figure>

***
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