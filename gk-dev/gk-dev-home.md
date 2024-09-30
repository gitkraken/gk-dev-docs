---

title: GitKraken.dev Support Home
description: Learn how to work with gitkraken.dev features
taxonomy:
    category: gk-dev

---

 GitKraken.dev is your command center for understanding the status of your development projects and teams. See pull requests and issues relevant to you, gain clear insights into your workflows, collaborate with your team, and begin working all within a browser via desktop or mobile. In addition to working with repositories, you can manage your Organization, Subscription and Security Controls. 

<img src="/wp-content/uploads/gkd-main-0.png" class="img-responsive center img-bordered"> 

***

## Launchpad

The Launchpad provides you with a summary of pull requests and issues relevant to you for the filtered selection and allows you to take action on these items. Instead of hunting for these pieces of information separately, you can get a holistic view of what you’re working on. To begin working with the Launchpad, start by connecting an [integration](/gk-dev/gk-dev-integrations/) to see your issues and pull requests. 

<img src="/wp-content/uploads/gkd-focus-view.png" class="img-responsive center img-bordered"> 

### Launchpad Actions

From the Launchpad you can begin working with pull requests and issues by taking actions on them from the actions column. Quickly update pull request or issue fields, open branches in GitKraken Desktop or VS Code, merge or close pull requests, open [code suggestions](/gk-dev/gk-dev-home/#code-suggest), and much more. 

<img src="/wp-content/uploads/gkd-take-action.png" class="img-responsive center img-bordered"> 

### Organizing the Launchpad

To change or narrow down your items shown, use the filters under the search bar. Select the desired service for your pull requests and issues, show only items where you are assigned/created/mentioned, or filter further based on [workspaces](/gk-dev/gk-dev-home/#workspaces). 

<img src="/wp-content/uploads/gkd-launchpad-filter.png" class="img-responsive center img-bordered"> 

To organize further, items in the Launchpad can be pinned, to move the item to the top of the list, and can be snoozed, to be hidden under the SNOOZED section. To pin or unpin and item, click the pin <i class="fa-solid fa-thumbtack"></i> in the pin column. To snooze an item, hover over an item, select the snooze <i class="fa-solid fa-snooze"></i> icon, and select the desired time option - selecting snooze will snooze the item until it is manually unsnoozed. To unsnooze an item, click on the `SNOOZED` section header, hover over the desired item and select the unsnooze icon for that item.

<img src="/wp-content/uploads/gkd-pin-or-snooze.gif" class="img-responsive center img-bordered"> 

***

## Cloud Patches

A Cloud Patch is a Git patch that GitKraken securely stores for you so it can be easily shared with others across GitKraken Desktop, GitLens, and the GitKraken CLI. The patch is directly transferred from your machine into secure storage or on your own [AWS S3 bucket](/gk-dev/gk-dev-security-controls/#self-hosted). Cloud Patches allow the ability to engage early with your team before a pull request.

### Creating a Cloud Patch

They can be created from [GitKraken Desktop](/gitkraken-client/experimental-features/#cloud-patches), [GitLens](gitlens/gitlens-features/#cloud-patches-preview), and the [GitKraken CLI](/cli/cli-home/#cloud-patches). From gitkraken.dev you can manage all Cloud Patches, including ones that have been shared with you.

<img src="/wp-content/uploads/gkd-cloud-patch-view.png" class="img-responsive center img-bordered"> 

### Working with Cloud Patches

Select `Open` to view the files and diffs included in the Cloud Patch. From here, you can open the Cloud Patch in [GitKraken Desktop](/gitkraken-client/experimental-features/#cloud-patches) or [GitLens](gitlens/gitlens-features/#cloud-patches-preview) to then apply the Cloud Patch to a specific branch.

<img src="/wp-content/uploads/gkd-open-cloud-patch.png" class="img-responsive center img-bordered"> 

***

## Workspaces

GitKraken Workspaces allow you to create easily accessible groups of repositories and share them with your organization members or [teams](/gk-dev/gk-dev-organization/#teams) to work with in gitkraken.dev, [GitKraken Desktop](/gitkraken-client/workspaces/), [GitLens](/gitlens/side-bar/#workspaces-☁%ef%b8%8f), and the [GitKraken CLI](/cli/cli-home/#create-workspaces-to-group-repos). 

<img src="/wp-content/uploads/gkd-workspaces-view.png" class="img-responsive center img-bordered"> 

### Creating a Workspace

To create a workspace, first connect the [integration](/gk-dev/gk-dev-integrations/) for the desired service. Once connected, select `Create Workspace`, provide a name, select a provider, and optionally provide a photo, description, or share with teams or members. 

<img src="/wp-content/uploads/gkd-create-workspace.png" class="img-responsive center img-bordered"> 

### Working with Workspaces

Select `Open Launchpad` to filer the Launchpad by the selected workspace for pull requests and issues. Additionally, workspaces can be used in [GitKraken Desktop](/gitkraken-client/workspaces/), [GitLens](/gitlens/side-bar/#workspaces-preview), and the [GitKraken CLI](/cli/cli-home/#create-workspaces-to-group-repos) to perform actions on multiple repositories, view repositories status at a glance, and much more. 

<img src="/wp-content/uploads/gkd-open-workspace.png" class="img-responsive center img-bordered"> 

### Requirement for Azure Workspaces and Insights

In order to work with Workspaces and [Insights](/gk-dev/gk-dev-insights) for Azure, `Third-party application access via OAuth` will need to be enabled in Azure from `Organization Settings > Policies`. You can find more information on this setting [here](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

***

## Code Suggest

GitKraken Code Suggest simplifies code review by allowing you to make suggestions and edits across the entire project, not just on the lines that were changed, within gitkraken.dev, GitLens, and GitKraken Desktop. When a Pull Request is open, you can make suggestions to the pull request that others can then review and accept to include in the pull request. 

<img src="/wp-content/uploads/cli-code-suggest.png" class="img-responsive center img-bordered"> 

### Working with Code Suggestions

Code Suggestions can be created from [GitKraken Desktop](/gitkraken-client/pull-requests/#review-code-and-suggest-changes), [GitLens](gitlens/gitlens-features/#code-suggest-preview), and the [GitKraken CLI](/cli/cli-home/#code-suggest) - see linked Help Center documentation for creating and working with them in each. 

Once a suggestion is created, it will include a comment on the pull request with two options: you can select _Code Suggestion for #PR_ to open the suggestion in gitkraken.dev or select _locally on your machine_ to open the suggestion in GitKraken or GitLens.

<img src="/wp-content/uploads/gl-code-suggest-comment.png" class="img-bordered img-responsive center">

When selecting the _Code Suggestion for #PR_ you will be taken to gitkraken.dev to review and accept the changes. Here, you can review the changes by selecting each file and once you are ready, you can select _Commit Suggestions_. This will create a new commit on the remote for the existing branch (shown under _COMMIT SUGGESTIONS TO_). 

<img src="/wp-content/uploads/gl-accept-code-suggestion.gif" class="img-bordered img-responsive center">



