---

title: gitkraken.dev
description: Learn how to work with gitkraken.dev
taxonomy:
    category: gk-dev

---

GitKraken.dev offers many of the GitKraken developer collaboration tools all within a browser via desktop or mobile. In addition, it allows you to manage Security Controls for users within your [GitKraken Organization](/gitkraken-client/gitkraken-organization/). 

<img src="/wp-content/uploads/gkd-main.png" class="img-responsive center img-bordered"> 

***

## Launchpad

The Launchpad will provide you with a summary of pull requests and issues relevant to you for the filtered selection as well as allow you to take action on these items. Instead of hunting for these pieces of information separately, you can get a holistic view of what you’re working on.

<img src="/wp-content/uploads/gkd-focus-view.png" class="img-responsive center img-bordered"> 

There is a search bar and filters to limit the issues and pull requests shown. Actions can be taken on issues and pull requests from the Actions column. Both can be opened on the connected service by selecting `Open`. Additionally, from the `Open` dropdown, pull requests can be opened in GitKraken Client, VS Code, and VS Code Insiders. 

Items in the Launchpad can be pinned, to move the item to the top of the list, and can be snoozed, to be hidden under the SNOOZED section. To pin or unpin and item, click the pin <i class="fa-solid fa-thumbtack"></i> in the pin column. To snooze an item, hover over an item, select the snooze <i class="fa-solid fa-snooze"></i> icon, and select the desired time option - selecting snooze will snooze the item until it is manually unsnoozed. To unsnooze an item, click on the `SNOOZED` section header, hover over the desired item and select the unsnooze icon for that item.

<img src="/wp-content/uploads/gkd-pin-or-snooze.gif" class="img-responsive center img-bordered"> 

***

## Cloud Patches

A Cloud Patch is a Git patch that GitKraken securely stores for you so it can be easily shared with others across GitKraken Client, GitLens, and the GitKraken CLI. The patch is directly transferred from your machine into secure storage or on your own [AWS S3 bucket](/gk-dev/gk-dev-home/#self-hosted).

Cloud Patches allow the ability to engage early with your team before a pull request. They can be created as soon as you have a work in progress. This can help with collaborating on changes prior to a pull request and minimize the delay of pull request reviews.

***

## Workspaces

GitKraken Workspaces allow you to create easily accessible groups of repositories and share them with your organization members or [teams](/gitkraken-client/gitkraken-organization/#teams) to work with in gitkraken.dev, [GitKraken Client](/gitkraken-client/workspaces/), [GitLens](/gitlens/side-bar/#workspaces-☁%ef%b8%8f), and the [GitKraken CLI](/cli/cli-home/#create-workspaces-to-group-repos). Additionally, Workspaces can be used to filter pull requests and issues in the Launchpad.

<img src="/wp-content/uploads/gkd-workspaces-view.png" class="img-responsive center img-bordered"> 

To create a workspace, first connect the [integration](/gk-dev/gk-dev-home/#integrations) for the desired service. Once connected, select `Create Workspace`, provide a name, select a provider, and optionally provide a photo, description, or share with teams or members. 

***

## Administration

Manage your organizations users, teams, subscription, security controls, or your own integrations. 

### Users

#### Add Users

To add someone to your organization select "Users" and then "Add Users". Here you can enter as many email addresses as you want and the [role](/gitkraken-client/gitkraken-organization/#roles) (in the drop down) you would like to assign them all. 

<img src="/wp-content/uploads/gkd-add-users.png" class="img-responsive center img-bordered">

Only members that have a [role](/gitkraken-client/gitkraken-organization/#roles) with permission can add users to an organization. When you do add someone, it will consume a license of your subscription. If all available licenses are consumed when adding a user, a billing summary will show up during the process, select "Purchase licenses & Add X User(s)" to complete the transaction and add the users.

<img src="/wp-content/uploads/gkd-add-and-purchase-user.png" class="img-responsive center img-bordered">

#### Reallocate Licenses

Any Owner, Admin, or Billing Contact may remove users and then add users to reallocate licenses.

The Billing Contact role cannot remove or edit Owner or Admin users.

To reallocate a license, navigate to Users and then select "Remove" for the desired user. Then, you can add the new user. 

#### Roles

Roles grant members permissions within an organization. There are four roles a user may have:
+ Owner: there must be exactly one owner per organization. Owners have full permission and consume a license.
+ Admin: Admins have full permissions and consume a license. Admins cannot remove or edit the owner.
+ User: Users have no administrative permissions but do consume a license.
+ Billing Contact: Billing Contacts have the same permissions as admins, except they do not consume a license.

<table class='table table--bordered table--shortcuts'>
    <thead>
        <tr>
            <th>Permission</th>
            <th>Owner</th>
            <th>Admin</th>
            <th>User</th>
            <th>Billing Contact</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Licensed to use GitKraken</td>
            <th>✅</th>
            <th>✅</th>
            <th>✅</th>
            <th></th>
        </tr>
        <tr>
            <td>Add, edit, and remove users</td>
            <th>✅</th>
            <th>✅</th>
            <th></th>
            <th>✅</th>
        </tr>
        <tr>
            <td>Create and manage teams</td>
            <th>✅</th>
            <th>✅</th>
            <th></th>
            <th>✅</th>
        </tr>
        <tr>
            <td>Manage billing and purchase licenses</td>
            <th>✅</th>
            <th>✅</th>
            <th></th>
            <th>✅</th>
        </tr>
        <tr>
            <td><a href="/gitkraken-client/gitkraken-organization/#transfer-ownership">Transfer ownership</a> of the organization</td>
            <th>✅</th>
            <th></th>
            <th></th>
            <th></th>
        </tr>
    </tbody>
</table>

***

### Teams

Teams are the best way to organize members of your GitKraken organization. In addition, teams can create Shared Workspaces to bring focus to their collaborative work and help [identify conflicts in GitKraken Client](/gitkraken-client/working-with-repositories/team-view/) by showing what files and branches your team is working on. Any member can create a team by visiting the Teams or within [GitKraken Client](/gitkraken-client/teams/). 

<img src="/wp-content/uploads/gkd-teams.png" class="img-responsive center img-bordered"> 

To create a Team, select `Create team`, provide a name, and select the desired users. 

<img src="/wp-content/uploads/gkd-create-team.png" class="img-responsive center img-bordered"> 

### Subscription

Subscriptions are tied directly to an [organization](/gitkraken-client/gitkraken-organization/), even if the subscription is for one user. The subscription is identical for everyone in the organization and one license is required for every member (unless their [role](/gitkraken-client/gitkraken-organization/#roles) does not use a license).

<img src="/wp-content/uploads/gkd-subscription-view.png" class="img-responsive center img-bordered"> 

#### How to Purchase

To purchase a subscription for the first time follow these steps:

1. Visit [gitkraken.dev/purchase-subscription](https://gitkraken.dev/purchase-subscription).
2. Login with your [GitKraken account](/gitkraken-client/gitkraken-account/) or create an account.
3. Select the tier that is best for your organization (Pro, Teams, or Enterprise) and the number of User Seats (one for each member of the organization that will be using the product). There are links at the bottom of each while can further elaborate on the differences.
4. Provide an Organization name, First Name, Last name, and Country. You can also provide a promo code if you have one.
5. Fill out or select the desired payment method.
6. Select the "<span style='color: green;'>Review your order Purchase</span>" button to complete your transaction.
7. If you added more licenses than there are members in the organization to claim, you will be taken to the "Add Users" screen.

<div class='callout callout--basic'>
   	<p>If you encounter trouble while purchasing and you have verified your payment method, please don’t hesitate to <a href="https://www.gitkraken.com/billing-issues">contact us</a> for support.</p>
</div>

#### Manage

If you have an existing subscription you can manage it from [gitkraken.dev/subscription](https://gitkraken.dev/subscription). This is where you can view, manage, and edit the subscription. 

#### Cancel

You can cancel your subscription at any time. To do so, login to [gitkraken.dev](https://gitkraken.dev/), select "Subscription" on the left side, and select "<span style='color: yellow;'>Cancel</span>." Follow the flow to complete cancellation. Once canceled, you will keep your subscription for the remainder of its billing period. Once the period is up, everyone in the organization will lose access to the subscription.

When your subscription is set to cancel but you can still use it, your organization will be labeled as "<span style='color: red;'>non-renewing</span>." When your subscription is completely canceled and the billing period has passed, it will be labeled as "<span style='color: red;'>canceled</span>."

<div class='callout callout--basic'>
   	<p>Only the owner, admins, and billing contacts have permission to cancel.</p>
</div>

#### Reactivation

You can always reactivate a canceled subscription. You can reactivate by logging into [gitkraken.dev](https://gitkraken.dev), select "Subscription" on the left side, and select "<span style='color: green;'>Keep GitKraken</span>." Please note the two cases.

#### Edit Billing

To update your billing method, go to [gitkraken.dev](https://gitkraken.dev), select "Subscription" on the left side, and click `Update `. From here you may select to update your existing payment method or switch between payment methods.

#### Billing History

Each billing cycle, the owner and billing contacts of the organization will receive an email with the receipt attached. If you would like to receive prior receipts, please contact [accounting](https://www.gitkraken.com/billing-issues) for additional copies.

### Settings

#### Integrations

To begin working with the Launchpad and Workspaces, start by connecting an integration from https://gitkraken.dev/settings/integrations. To connect an integration, select the desired integration under **Add Integration**.

- For Cloud integrations: Log in to the desired account and then approve access for GitKraken.
- For Self-Hosted/Server integrations: Fill out Host Domain, select `Generate a token on {service}` - this will open the service on the PAT creation page with the required scopes, fill out the PAT and then select `Connect`.

<img src="/wp-content/uploads/gkd-integrations-0.png" class="img-responsive center img-bordered"> 

<div class='callout callout--basic'>
   	<p>Note for GitHub.com: In order to work with repositories owned by a GitHub organization, the organization will need to allow <a href="https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/">Organization Approval</a> for GitKraken.</p>
</div>

##### AI features

The GitKraken suite includes a lineup of AI features that are intended to speed up your workflow. These features require sending some of your code to an AI hosted on the cloud such as ChatGPT. If you are concerned that AI features do not comply with your company’s data security, you can disable AI features for everyone in your organization. Please note that changing this setting requires you to have the role [owner, admin, or billing contact](/gitkraken-client/gitkraken-organization/#roles) on a [Teams or Enterprise plan](https://www.gitkraken.com/pricing).

##### Cloud Patches

Allow developers in your organization to create Cloud Patches that can be shared with others. A Cloud Patch is a Git patch that is stored securely by GitKraken. If you are concerned that Cloud Patches do not comply with your company’s data security, you can set up self-hosted Cloud Patches for your organization. If this is not an option for you, please [contact our customer success team](https://www.gitkraken.com/sales-inquiries).

##### Self-hosted

You can host your organization’s Cloud Patches on your own AWS S3 bucket. To do so login to https://gitkraken.dev/settings/security, copy the bucket policy by clicking “Copy policy.” Open the AWS Console and navigate to the S3 service. From there, click on the bucket you want to store Cloud Patches. Click the "Permissions" tab and look for the “Bucket policy" section. Click the "Edit" button and paste the bucket policy into the text box. Rename CUSTOMER_BUCKET_NAME with the name of your bucket. Finally, click "Save changes” and return to https://gitkraken.dev/settings/security to test your bucket.

Please note to setup self-hosted Cloud Patches require you to have the role [owner, admin, or billing contact](/gitkraken-client/gitkraken-organization/#roles) on an [Enterprise plan](https://www.gitkraken.com/pricing).

<img src="/wp-content/uploads/gkd-self-hosted-bucket.png" class="img-responsive center img-bordered"> 