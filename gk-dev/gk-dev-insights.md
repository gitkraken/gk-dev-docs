---
title: Getting Started with GitKraken Insights
description: Learn how to request access, understand plan availability, and connect your data in GitKraken Insights.
taxonomy:
    category: gk-dev
---
<kbd>Last updated: February 2026</kbd>

GitKraken Insights turns raw Git data into clear, useful metrics for developers and leaders. It pulls code activity, pull requests, issues, and CI/CD results into a single view that fits directly into existing workflows.

Instead of surface-level stats, Insights shows how work connects to team goals and points out ways to improve flow and productivity.

<figure>
  <img src="/wp-content/uploads/insights-dashboard-oct-2025.png" srcset="/wp-content/uploads/insights-dashboard-oct-2025@2x.png" class="help-center-img img-bordered" alt="Dashboard view showing GitKraken Insights metrics, including deployment frequency, code duplication, PR response time, and code rework trends over a 30-day period." />
  <figcaption style="text-align: center; color: #888">Overview of GitKraken Insights</figcaption>
</figure>

---

## Request Access

GitKraken Insights is available by request only. To get started, [request a guided tour](https://www.gitkraken.com/insights#form).  

 A member of the GitKraken team will contact you right away to walk you through Insights and explain how to enable access for your organization.

**Note:** Insights is available as an add-on to the seats in your existing GitKraken subscription, or as a discounted standalone solution for developers on your team who don't use GitKraken.

---

## Connecting your data

Once your access is approved, you can connect Insights to your repositories and configure settings for your organization.  

Currently, Insights supports connections with GitHub, GitLab, Bitbucket and Jira Cloud. Support for Azure DevOps is coming soon. 

In addition, you can connect AI providers to enable AI Impact insights (like Duplicated Code, Prompt Acceptance Rate, and more).
---

### 1. Repo import

1. In GitKraken.dev, go to **Insights > Data Connection**.  
2. Click to connect with GitHub, GitLab, Cursor, GitHub CoPilot, Azure Devops, Bitbucket or Jira Cloud.  
3. Authorize GitKraken Insights by GitClear to connect with GitHub.  
4. Select which repositories to track. Use the filter option at the top of the page to quickly narrow down the list.  


<figure>
  <img src="/wp-content/uploads/data-connection-dec-2025.png" srcset="/wp-content/uploads/data-connection-dec-2025@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights data connections screen showing integration status and options to connect GitHub, GitLab, Bitbucket, and other tools." />
  <figcaption style="text-align: center; color: #888">Connect GitHub, GitLab,Bitbucket or Jira to enable Insights</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/authorize-gitclear.png" srcset="/wp-content/uploads/authorize-gitclear@2x.png" class="help-center-img img-bordered" alt="GitHub authorization screen for GitKraken Insights by GitClear, showing requested access permissions including repositories, teams, and Copilot." />
  <figcaption style="text-align: center; color: #888">Authorize GitHub access for GitKraken Insights</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/import-repos.png" srcset="/wp-content/uploads/import-repos@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights interface for selecting and importing repositories, with a quick import field and a list of user repos to choose from." />
  <figcaption style="text-align: center; color: #888">Select which repos to import. You can always import more later.</figcaption>
</figure>

#### Avoiding GitHub API rate limits

If you're importing a large number of repositories—depending on size and commit history—you may encounter GitHub's hourly API rate limits. This can temporarily throttle other GitHub services used by your organization.

To avoid this, additional members of your organization can connect to Insights using a [Lead role](/gk-dev/gk-dev-organization/#roles). When multiple people are connected, the app distributes processing across their GitHub tokens to help avoid throttling.

After the initial import is complete, rate limit issues are unlikely to recur.


---

#### AI Provider Connection (Optional)

As of December 2025, GitKraken Insights only supports connections with Cursor and GitHub Copilot to enable AI insights.

To enable AI Impact insights, connect your preferred AI provider:
1. In GitKraken.dev, go to [**Insights > Data Connection**](https://gitkraken.dev/insights/data-connections).
2. Click to `Manage` with Cursor or Github Copilot.
3. In the new window, select the AI provider you wish to connect with and enter the provider Token.
4. Click **Connect AI Provider** to finish the connection.
<figure>
  <img src="/wp-content/uploads/gk-dev-ai-provider-connection.png" srcset="/wp-content/uploads/gk-dev-ai-provider-connection@2x.png" class="help-center-img img-bordered" alt="Screenshot of AI provider connection" />
  <figcaption style="text-align: center; color: #888">Connect your AI provider to enable AI Impact insights</figcaption>
</figure>

### 2. Setup role

After connecting repositories, confirm your personal details:

- First and last name  
- Time zone  
- Job role  

<figure>
  <img src="/wp-content/uploads/set-role-oct-2025.png" srcset="/wp-content/uploads/set-role-oct-2025@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights onboarding screen prompting the user to enter their first name, last name, time zone, and job title before continuing." />
  <figcaption style="text-align: center; color: #888">Confirm your details before continuing</figcaption>
</figure>


---

### 3. Data import progress

Once setup is complete, Insights will begin importing your repository data.  

- Expect **past month’s activity** to appear within a few hours.  
- Full **year’s activity** is usually ready within one to two days.  
- Track import progress anytime from the **Dashboard** tab.  

<figure>
  <img src="/wp-content/uploads/import-progress.png" srcset="/wp-content/uploads/import-progress@2x.png" class="help-center-img img-bordered" alt="GitKraken Insights data import progress screen with options to manage teams, releases, and users, alongside an illustration of the GitKraken mascot loading data." />
  <figcaption style="text-align: center; color: #888">Monitor import progress while Insights processes your data</figcaption>
</figure>