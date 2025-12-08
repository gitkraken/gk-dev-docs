---
title: Getting Started with GitKraken Insights
description: Learn how to request access, understand plan availability, and connect your data in GitKraken Insights.
taxonomy:
    category: gk-dev
---
<kbd>Last updated: December 2025</kbd>

GitKraken Insights turns raw Git data into clear, useful metrics for developers and leaders. It pulls code activity, pull requests, issues, and CI/CD results into a single view that fits directly into existing workflows.

Instead of surface-level stats, Insights shows how work connects to team goals and points out ways to improve flow and productivity.

<figure>
  <img src="/wp-content/uploads/insights-dashboard-oct-2025.png" srcset="/wp-content/uploads/insights-dashboard-oct-2025@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
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

Currently, Insights supports connections with GitHub, GitLab and Jira Cloud. Support for Bitbucket and Azure DevOps is coming soon. 

---

### 1. Repo import

1. In GitKraken.dev, go to **Insights > Data Connection**.  
2. Click to connect with GitHub, GitLab, or Jira Cloud.  
   > Support for Bitbucket and Azure DevOps, is coming soon.  
3. Authorize GitKraken Insights by GitClear to connect with GitHub.  
4. Select which repositories to track. Use the filter option at the top of the page to quickly narrow down the list.  


<figure>
  <img src="/wp-content/uploads/data-connection-oct-25.png" srcset="/wp-content/uploads/data-connection-oct-25@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Connect GitHub, GitLab, or Jira to enable Insights</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/authorize-gitclear.png" srcset="/wp-content/uploads/authorize-gitclear@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Authorize GitHub access for GitKraken Insights</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/import-repos.png" srcset="/wp-content/uploads/import-repos@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Select which repos to import. You can always import more later.</figcaption>
</figure>

#### Avoiding GitHub API rate limits

If you're importing a large number of repositories—typically over 100, depending on size and commit history—you may encounter GitHub's hourly API rate limits. This can temporarily throttle other GitHub services used by your organization.

To avoid this, additional members of your organization can connect to Insights using a [Lead role](/gk-dev/gk-dev-organization/#roles). When multiple Leads are connected, GitClear distributes processing across their GitHub tokens to help avoid throttling.

After the initial import is complete, rate limit issues are unlikely to recur.


---

### 2. Setup role

After connecting repositories, confirm your personal details:

- First and last name  
- Time zone  
- Job role  

<figure>
  <img src="/wp-content/uploads/set-role-oct-2025.png" srcset="/wp-content/uploads/set-role-oct-2025@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Confirm your details before continuing</figcaption>
</figure>


---

### 3. Data import progress

Once setup is complete, Insights will begin importing your repository data.  

- Expect **past month’s activity** to appear within a few hours.  
- Full **year’s activity** is usually ready within one to two days.  
- Track import progress anytime from the **Dashboard** tab.  

<figure>
  <img src="/wp-content/uploads/import-progress.png" srcset="/wp-content/uploads/import-progress@2x.png" class="help-center-img img-bordered" alt="Overview of GitKraken Insights" />
  <figcaption style="text-align: center; color: #888">Monitor import progress while Insights processes your data</figcaption>
</figure>