---

title: GitKraken.dev Administration
description: Learn how to work with administrative features on GitKraken.dev
taxonomy:
    category: gk-dev

---

Administer your Organization, Users, Teams, Subscription, and security controls on gitkraken.dev. 

***

## GitKraken Account

Your GitKraken account is your key to unlock the most personal experience across GitKraken products.

### Login

You can create your GitKraken account at [gitkraken.dev](https://gitkraken.dev/register) or GitKraken Desktop. When presented with the login page, you may need to select “Create an account” before selecting how you would like to create your GitKraken account. There are seven options available to create your GitKraken account and login. You can choose your preferred hosting service (GitHub, GitLab, Bitbucket, and Azure DevOps), login with email, Google, or [SSO](/gitkraken-client/single-sign-on/).

<img src="/wp-content/uploads/gkd-log-in.png" class="img-responsive center img-bordered">

Once you have created your GitKraken account, your account is tied to the primary email address of whichever method you selected. If you use the “Sign up with Email” method, you will need to verify your email address with a link sent to your email.

### Manage Account

`Manage Account` can be accessed from the dropdown in the top right to do things like [personalize your account](/gitkraken-client/gitkraken-account/#personalization), start a [multi-user trial](/gitkraken-client/trials/#multi-user-trials), [set up SSO](/gitkraken-client/single-sign-on/) and [transfer the organization ownership](/gitkraken-client/gitkraken-organization/#transfer-ownership).

<img src="/wp-content/uploads/gkd-manage-account.png" class="img-responsive center img-bordered">

***

## Users

To add someone to your organization select "Users" and then "Add Users". Here you can enter as many email addresses as you want and the [role](/gitkraken-client/gitkraken-organization/#roles) (in the drop down) you would like to assign them all. 

<img src="/wp-content/uploads/gkd-add-user.png" class="img-responsive center img-bordered">

Only members that have a [role](/gk-dev/gk-dev-administration/#roles) with permission can add users to an organization. When you do add someone, it will consume a license of your subscription. If all available licenses are consumed when adding a user, a billing summary will show up during the process, select "Purchase licenses & Add X User(s)" to complete the transaction and add the users.

<img src="/wp-content/uploads/gkd-add-and-purchase-user.png" class="img-responsive center img-bordered">

### Inviting Users to Your Organization

As a User, you have the ability to invite other users to the organization for an Owner, Admin, or Billing Contact to approve and/or purchase a license for. 

To invite a user, navigate to gitkraken.dev > Users > Invite Users. Then provide the email(s) of the desired user(s). 

<img src='/wp-content/uploads/gkdev-invite-user-as-user.png' srcset='/wp-content/uploads/gkdev-invite-user-as-user@2x.png' class='img-bordered img-responsive center'>

This will send an email to any Owner, Admin, or Billing Contact to review the invited user. They can select `Review` on the email or see the invitees from gitkraken.dev > Users > Review. Here, they can Approve or Deny the user. If your organization is at its user limit, you will be prompted to purchase an additional license when approving.

<img src='/wp-content/uploads/gkdev-review-user-invite.png' srcset='/wp-content/uploads/gkdev-review-user-invite@2x.png' class='img-bordered img-responsive center'>

### Reallocate Licenses

Any Owner, Admin, or Billing Contact may remove users and then add users to reallocate licenses.

The Billing Contact role cannot remove or edit Owner or Admin users.

To reallocate a license, navigate to Users and then select "Remove" for the desired user. Then, you can add the new user. 

### Roles

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

## Teams

Teams are the best way to organize members of your GitKraken organization. In addition, teams are offered for a variety of collaborative features like [Shared Workspaces](/gk-dev/gk-dev-home/#workspaces), [Cloud patches](/gk-dev/gk-dev-home/#cloud-patches), [Code Suggest](/gk-dev/gk-dev-home/#code-suggest), and more to come.

<img src="/wp-content/uploads/gkd-teams.png" class="img-responsive center img-bordered"> 

To create a Team, select `Create team`, provide a name, and select the desired users. 

<img src="/wp-content/uploads/gkd-create-team.png" class="img-responsive center img-bordered"> 

***

## Subscription

Subscriptions are tied directly to an [organization](/gitkraken-client/gitkraken-organization/), even if the subscription is for one user. The subscription is identical for everyone in the organization and one license is required for every member (unless their [role](/gitkraken-client/gitkraken-organization/#roles) does not use a license).

<img src="/wp-content/uploads/gkd-subscription-view.png" class="img-responsive center img-bordered"> 

### How to Purchase

To purchase a subscription for the first time follow these steps:

1. Visit [gitkraken.dev/purchase-subscription](https://gitkraken.dev/purchase-subscription).
2. Login with your [GitKraken account](/gk-dev-home/#account) or create an account.
3. Select the tier that is best for your organization (Pro, Teams, or Enterprise) and the number of User Seats (one for each member of the organization that will be using the product). There are links at the bottom of each while can further elaborate on the differences.
4. Provide an Organization name, First Name, Last name, and Country. You can also provide a promo code if you have one.
5. Fill out or select the desired payment method.
6. Select the "<span style='color: green;'>Review your order Purchase</span>" button to complete your transaction.
7. If you added more licenses than there are members in the organization to claim, you will be taken to the "Add Users" screen.

<div class='callout callout--basic'>
   	<p>If you encounter trouble while purchasing and you have verified your payment method, please don’t hesitate to <a href="https://www.gitkraken.com/billing-issues">contact us</a> for support.</p>
</div>

### Manage

If you have an existing subscription you can manage it from [gitkraken.dev/subscription](https://gitkraken.dev/subscription). This is where you can view, manage, and edit the subscription. 

### Cancel

You can cancel your subscription at any time. To do so, login to [gitkraken.dev](https://gitkraken.dev/), select "Subscription" on the left side, and select "<span style='color: yellow;'>Cancel</span>." Follow the flow to complete cancellation. Once canceled, you will keep your subscription for the remainder of its billing period. Once the period is up, everyone in the organization will lose access to the subscription.

When your subscription is set to cancel but you can still use it, your organization will be labeled as "<span style='color: red;'>non-renewing</span>." When your subscription is completely canceled and the billing period has passed, it will be labeled as "<span style='color: red;'>canceled</span>."

<div class='callout callout--basic'>
   	<p>Only the owner, admins, and billing contacts have permission to cancel.</p>
</div>

### Reactivation

You can always reactivate a canceled subscription. You can reactivate by logging into [gitkraken.dev](https://gitkraken.dev), select "Subscription" on the left side, and select "<span style='color: green;'>Keep GitKraken</span>." 

### Edit Billing

To update your billing method, go to [gitkraken.dev](https://gitkraken.dev), select "Subscription" on the left side, and click `Update`. From here you may select to update your existing payment method or switch between payment methods.

### Billing History

Each billing cycle, the owner and billing contacts of the organization will receive an email with the receipt attached. If you would like to receive prior receipts, please contact [accounting](https://www.gitkraken.com/billing-issues) for additional copies.

***

## Settings

### Integrations

To begin working with the Launchpad and Workspaces, start by connecting an integration from https://gitkraken.dev/settings/integrations. To connect an integration, select the desired integration under **Add Integration**.

- For Cloud integrations: Log in to the desired account and then approve access for GitKraken.
- For Self-Hosted/Server integrations: Fill out Host Domain, select `Generate a token on {service}` - this will open the service on the PAT creation page with the required scopes - fill out the PAT and then select `Connect`.

<img src="/wp-content/uploads/gkd-integrations-0.png" class="img-responsive center img-bordered"> 

<div class='callout callout--basic'>
   	<p>Note for GitHub.com: In order to work with repositories owned by a GitHub organization, the organization will need to allow <a href="https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/">Organization Approval</a> for GitKraken.</p>
</div>

### Security Controls 

#### AI features

The GitKraken suite includes a lineup of AI features that are intended to speed up your workflow. These features require sending some of your code to an AI hosted on the cloud such as ChatGPT. If you are concerned that AI features do not comply with your company’s data security, you can disable AI features for everyone in your organization. Please note that changing this setting requires you to have the role [owner, admin, or billing contact](/gk-dev-administration/#roles) on a [Teams or Enterprise plan](https://www.gitkraken.com/pricing).

#### Cloud Patches

Allow developers in your organization to create Cloud Patches that can be shared with others. A Cloud Patch is a Git patch that is stored securely by GitKraken. If you are concerned that Cloud Patches do not comply with your company’s data security, you can set up self-hosted Cloud Patches for your organization. If this is not an option for you, please [contact our customer success team](https://www.gitkraken.com/sales-inquiries).

#### Self-hosted

You can host your organization’s Cloud Patches on your own AWS S3 bucket. To do so login to https://gitkraken.dev/settings/security, copy the bucket policy by clicking “Copy policy.” Open the AWS Console and navigate to the S3 service. From there, click on the bucket you want to store Cloud Patches. Click the "Permissions" tab and look for the “Bucket policy" section. Click the "Edit" button and paste the bucket policy into the text box. Rename CUSTOMER_BUCKET_NAME with the name of your bucket. Finally, click "Save changes” and return to https://gitkraken.dev/settings/security to test your bucket.

Please note to setup self-hosted Cloud Patches require you to have the role [owner, admin, or billing contact](/gitkraken-client/gitkraken-organization/#roles) on an [Enterprise plan](https://www.gitkraken.com/pricing).

<img src="/wp-content/uploads/gkd-self-hosted-bucket.png" class="img-responsive center img-bordered"> 

### Organization

Your [GitKraken organization](/gitkraken-client/gitkraken-organization/) name can be renamed at any time by an Owner, Admin, or Billing Contact. To rename an organization, navigate to Settings, Organization, update the Organization Name, and then select `save`. 

<img src="/wp-content/uploads/gkd-organization-name.png" class="img-responsive center img-bordered"> 