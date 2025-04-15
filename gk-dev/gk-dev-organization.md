---

title: Manage GitKraken Organization
description: Learn about GitKraken Organizations
taxonomy:
    category: gk-dev
    
---

A GitKraken organization is a collection of [GitKraken accounts](/gk-dev/gk-dev-account/) which unlocks a shared [subscription](/gk-dev/gk-dev-subscription/), collaboration features between members, and administration of the members in the organization. If you are creating an account for the first time, an organization will automatically be created for you.
<div class='callout callout--warning'>
    <p>Community users are a single user plan, and can not perform any org management. Pro plans and above can perform Org management functions.</p>
</div>
***

## Add users

To add someone to your organization, go to [gitkraken.dev](https://gitkraken.dev/?source=help_center&product=gitkraken_dot_dev), select your organization dropdown in the top left, select "Users", and finally select "Add Users." 

<img src="/wp-content/uploads/gk-dev-add-user.png" srcset="/wp-content/uploads/gk-dev-add-user@2x.png" class="img-responsive center img-bordered">

Here you can enter as many email addresses as you want and the [role](/gk-dev/gk-dev-organization/#roles) (in the drop down) you would like to assign them all. 

<img src="/wp-content/uploads/gk-dev-add-user-modal.png" class="img-responsive center img-bordered">

Only members that have a [role](/gk-dev/gk-dev-organization/#roles) with permission can add users to an organization. When you do add someone, it will consume a license of your subscription. If all available licenses are consumed when adding a user, a billing summary will show up during the process, select "Purchase" to complete the transaction and add the users.

<img src="/wp-content/uploads/gk-dev-add-user-modal-2.png" class="img-responsive center img-bordered">

You can also add licenses in bulk to your organization separately from adding users by going to the [Subscription](/gk-dev/gk-dev-subscription/) section in your organization.

***

## Inviting users to your organization

As a User, you have the ability to invite other users to the organization for an Owner, Admin, or Billing Contact to approve and/or purchase a license for. 

To invite a user, navigate to gitkraken.dev > Users > Invite Users. Then provide the email(s) of the desired user(s). 

<img src='/wp-content/uploads/gkdev-invite-user-as-user.png' srcset='/wp-content/uploads/gkdev-invite-user-as-user@2x.png' class='img-bordered img-responsive center'>

This will send an email to any Owner, Admin, or Billing Contact to review the invited user. They can select `Review` on the email or see the invitees from gitkraken.dev > Users > Review. Here, they can Approve or Deny the user. If your organization is at its user limit, you will be prompted to purchase an additional license when approving.

<img src='/wp-content/uploads/gkdev-review-user-invite.png' srcset='/wp-content/uploads/gkdev-review-user-invite@2x.png' class='img-bordered img-responsive center'>

***

## Reallocate licenses

Any Owner, Admin, or Billing Contact may remove users and then add users to reallocate licenses.

The Billing Contact role cannot remove or edit Owner or Admin users.

To reallocate a license, navigate to Users and then select "Remove" for the desired user. Then, you can add the new user. 

***

## Import and export users

To import multiple users via CSV select the “Add User” button. From here you can select “Import via CSV”. When importing users, be sure to have columns for `Email`, `Username`, `Role`, `User License`.

<img src="/wp-content/uploads/gk-dev-import-users.png" class="img-responsive center img-bordered">

To export users to a CSV, select “Export via CSV”. The export will contain columns for Email, Username, Role, User License.

<img src="/wp-content/uploads/gk-dev-export-users.png" class="img-responsive center img-bordered">

***

## Roles

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
            <td><a href="/gk-dev/gk-dev-organization/#transfer-ownership">Transfer ownership</a> of the organization</td>
            <th>✅</th>
            <th></th>
            <th></th>
            <th></th>
        </tr>
    </tbody>
</table>

***

## Teams

Teams are the best way to organize members of your GitKraken organization. In addition, teams can create Shared Workspaces to bring focus to their collaborative work and help identify conflicts by showing what files and branches your team is working on.

Any member can create a team by visiting the Teams tab within the organization at [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken_dot_dev). For more information on creating and working with teams, see the [Teams](/gitkraken-desktop/teams/) page.

<img src='/wp-content/uploads/gk-dev-teams.png' srcset='/wp-content/uploads/gk-dev-teams@2x.png' class='img-bordered img-responsive center'>

***

## Organization Settings

Organization settings can be accessed from [gitkraken.dev/settings/organization](https://gitkraken.dev/settings/organization?source=help_center&product=gitkraken_dot_dev). Visiting the Settings section of your organization will give you a snapshot of your subscription and allow you to edit a few key aspects of your organization like changing the organization name, transferring ownership of the organization, leaving an organization, and setting up single sign-on.

<img src="/wp-content/uploads/gk-dev-organization-settings.png" srcset='/wp-content/uploads/gk-dev-organization-settings@2x.png' class="img-responsive center img-bordered">

### Transfer ownership

If you’re the [owner](/gk-dev/gk-dev-organization/#roles) of an organization and would like to make someone else the owner you can do that. First you need to make sure to first add that account to the organization. Once the account is added to your organization, go to your organization, select "Settings" and then “Transfer ownership.” You will select the user within the organization to become the owner (and type their email to confirm). Once you select “Transfer Ownership,” the transfer is final and cannot be undone unless the new owner transfers ownership back to the original owner.

<img src="/wp-content/uploads/gk-dev-transfer-owner.gif" class="img-responsive center img-bordered">

### Leave an organization

If you no longer need to be a part of an organization, you can leave an organization by navigating to Settings, then Organization and then `Leave Organization`. If you leave an organization, only an admin can invite you back. You will lose access to collaboration with members of GitKraken and your GitKraken paid license. 

This option will only be available if you are part of another organization and you are not the owner of the organization. If you are the current owner, you can [transfer the ownership](/gk-dev/gk-dev-organization/#transfer-ownership) and then leave the organization after.

<img src='/wp-content/uploads/gk-dev-leave-organization.png' srcset='/wp-content/uploads/gk-dev-leave-organization@2x.png' class='img-bordered img-responsive center'>

### Single sign-on

Single sign-on (SSO) is available for organizations that require it. See how to setup SSO by visiting our [Single Sign-On documentation](/gk-dev/gk-dev-single-sign-on/).

