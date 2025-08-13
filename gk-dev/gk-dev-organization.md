---
title: Manage GitKraken Organizations | Roles, Users, Teams, SSO
description: Learn how to manage GitKraken organizations, assign roles, add users, configure teams, and set up SSO.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

Create an organization in GitKraken.dev to manage your team’s access, roles, licenses, and SSO. Centralize your GitKraken [subscription](/gk-dev/gk-dev-subscription/) to simplify provisioning and oversight across all GitKraken products.

<div class='callout callout--warning'>
    <p>Community users are on a single-user plan and cannot perform any organization management. Pro plans and higher can manage users, roles, teams, and settings.</p>
</div>

***

## Roles

Roles determine what permissions a member has within your organization. There are four roles available:

- **Owner** – Each organization has one owner by default. The owner has full administrative and billing permissions and consumes a license.
- **Admin** – Has full administrative and billing permissions and consumes a license. Admins cannot change or remove the owner.
- **User** – Has access to GitKraken features but no administrative permissions. This role consumes a license.
- **Billing Contact** – Manages billing-related settings and receives invoices. This role does not consume a license.

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

## Add users

To add someone to your organization, go to [gitkraken.dev](https://gitkraken.dev/?source=help_center&product=gitkraken_dot_dev), open the organization dropdown in the top left, select **Users**, then click **Add Users**.

<figure>
  <img src="/wp-content/uploads/gk-dev-add-user.png" srcset="/wp-content/uploads/gk-dev-add-user@2x.png" class="img-bordered center help-center-img" alt="Add Users screen in GitKraken">
  <figcaption style="color:#888;text-align:center">Access the Add Users screen from the Users tab</figcaption>
</figure>

You can enter multiple email addresses and select the [role](/gk-dev/gk-dev-organization/#roles) from the dropdown to assign to all users.

<figure>
  <img src="/wp-content/uploads/gk-dev-add-user-modal.png" class="img-bordered center help-center-img" alt="Add users modal with email and role fields">
  <figcaption style="color:#888;text-align:center">Enter emails and assign a role to each new user</figcaption>
</figure>

Only members with a [role](/gk-dev/gk-dev-organization/#roles) that includes user management permissions can invite others. Adding a user consumes a license from your subscription. If you exceed your license count during this step, a billing summary will appear. Select **Purchase** to complete the transaction and add the users.

<figure>
  <img src="/wp-content/uploads/gk-dev-add-user-modal-2.png" class="img-bordered center help-center-img" alt="Modal showing additional license purchase required">
  <figcaption style="color:#888;text-align:center">Purchase additional licenses if needed when adding users</figcaption>
</figure>

You can also purchase extra licenses in advance from the [Subscription](/gk-dev/gk-dev-subscription/) section.

***

## Inviting users to your organization

As a **User**, you can invite others to your organization. These invitations must be reviewed and approved by an Owner, Admin, or Billing Contact.

To invite someone:

1. Go to [gitkraken.dev](https://gitkraken.dev/?source=help_center&product=gitkraken_dot_dev)
2. Select your organization from the top-left dropdown
3. Navigate to **Users > Invite Users**
4. Enter the email address(es) of the person you want to invite

<figure>
  <img src='/wp-content/uploads/gkdev-invite-user-as-user.png' srcset='/wp-content/uploads/gkdev-invite-user-as-user@2x.png' class='img-bordered center help-center-img' alt='User invite screen in GitKraken'>
  <figcaption style='color:#888;text-align:center'>Submit user invitations for approval</figcaption>
</figure>

Once submitted, Owners, Admins, or Billing Contacts will receive an email notification. They can click **Review** from the email or go to **Users > Review** in the GitKraken interface to approve or deny the invitation. If your organization is at its user limit, approving an invite may prompt a license purchase.

<figure>
  <img src='/wp-content/uploads/gkdev-review-user-invite.png' srcset='/wp-content/uploads/gkdev-review-user-invite@2x.png' class='img-bordered center help-center-img' alt='Review and approve user invitation interface'>
  <figcaption style='color:#888;text-align:center'>Approvers can approve, deny, or assign licenses to new users</figcaption>
</figure>

***

## Reallocate licenses

Owners, Admins, and Billing Contacts can remove existing users to free up licenses, then add new users in their place.

> **Note:** Billing Contacts cannot remove or edit Owner or Admin users.

To reallocate a license:

1. Navigate to **Users**
2. Click **Remove** next to the user you want to remove
3. Invite or add a new user to use the available license

***

## Import and export users

To import multiple users via CSV, click the **Add Users** button, then choose **Import via CSV**. Be sure your file includes the following columns: `Email`, `Username`, `Role`, `User License`, and optionally `Teams`.

### User Import CSV Format

Your CSV file should include these columns:

| Column | Required | Description |
|--------|----------|-------------|
| Email | Yes | User's email address |
| Username | Yes | User's username |
| Role | Yes | User's role (Owner, Admin, User, or Billing Contact) |
| Teams | No | Teams to add the user to (separate multiple teams with semicolons) |

**Example CSV for user import:**
```csv
Email,Username,Role,Teams
john.doe@gitkiraken.com,johndoe,user,Frontend Team;Design Team
jane.smith@gitkiraken.com,janesmith,admin,Backend Team
bob.wilson@gitkiraken.com,bobwilson,user,Frontend Team
ashton.kutcher@gitkiraken.com,ashtonkutcher,user,Design Team
constance.baker@gitkiraken.com,constancebaker,user,Design Team
```

> **Note:** When you include teams in the CSV, these must already exist. Otherwise, gitkraken.dev will ignore the teams column. A single semicolon is used to separate multiple teams.

<figure>
  <img src="/wp-content/uploads/gk-dev-import-users.png" class="img-bordered center help-center-img" alt="CSV import modal in GitKraken">
  <figcaption style="color:#888;text-align:center">Import multiple users via a formatted CSV file</figcaption>
</figure>

To export your current user list to CSV, click **Export via CSV**. The export will include columns for Email, Username, Role, User License, and Teams.

<figure>
  <img src="/wp-content/uploads/gk-dev-export-users.png" class="img-bordered center help-center-img" alt="CSV export button in GitKraken">
  <figcaption style="color:#888;text-align:center">Export a CSV of your organization's members</figcaption>
</figure>

***

## Teams

Teams help you organize members within your GitKraken organization. Teams can also create Shared Workspaces to stay aligned on collaborative work and avoid merge conflicts by seeing what files and branches team members are working on.

Any member can create a team from the **Teams** tab in your organization at [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken_dot_dev). For details on creating and working with teams, visit the [Teams](/gitkraken-desktop/teams/) documentation.

### Bulk Import Teams

To import multiple teams via CSV, go to the **Teams** tab and click **Create Team**, then choose **Import via CSV**. This allows you to create multiple teams at once and optionally add existing users to those teams.

#### Team Import CSV Format

Your CSV file should include these columns:

| Column | Required | Description |
|--------|----------|-------------|
| Team Name | Yes | Name of the team to create |
| Users | No | Existing users to add to the team (separate multiple users with semicolons) |

**Example CSV for team import:**
```csv
Team,Emails
Frontend Team,bob.wilson@gitkiraken.com;john.doe@gitkiraken.com
Backend Team,jane.smith@gitkiraken.com
Design Team,ashton.kutcher@gitkiraken.com;constance.baker@gitkiraken.com;john.doe@gitkiraken.com
```

> **Note:** The Users column is optional. If you include users, GitKraken will add existing users to the teams. Multiple users can be specified in a single cell by separating them with semicolons. Teams will be created if they don't already exist.

<figure>
  <img src='/wp-content/uploads/gk-dev-teams.png' srcset='/wp-content/uploads/gk-dev-teams@2x.png' class='img-bordered center help-center-img' alt='GitKraken organization teams interface'>
  <figcaption style='color:#888;text-align:center'>Use teams to organize members and collaborate efficiently</figcaption>
</figure>

***

## Organization Settings

Access your settings at [gitkraken.dev/settings/organization](https://gitkraken.dev/settings/organization?source=help_center&product=gitkraken_dot_dev). From here, you can view subscription details and update:

- Organization name
- Ownership
- SSO setup
- Organization membership

<figure>
  <img src="/wp-content/uploads/gk-dev-organization-settings.png" srcset='/wp-content/uploads/gk-dev-organization-settings@2x.png' class="img-bordered center help-center-img" alt="Organization settings page">
  <figcaption style="color:#888;text-align:center">Update organization settings including name, ownership, and SSO</figcaption>
</figure>

### Transfer ownership

If you’re the [owner](/gk-dev/gk-dev-organization/#roles) of an organization and want to assign ownership to someone else:

1. Make sure the new owner is already added to the organization
2. Go to **Settings > Transfer ownership**
3. Select the user and confirm their email
4. Click **Transfer Ownership** to finalize the change

> **Note:** Ownership transfers are final unless the new owner reassigns it.

<figure>
  <img src="/wp-content/uploads/gk-dev-transfer-owner.gif" class="img-bordered center help-center-img" alt="Transfer ownership workflow">
  <figcaption style="color:#888;text-align:center">Transfer organization ownership to another member</figcaption>
</figure>

### Leave an organization

To leave an organization:

1. Navigate to **Settings > Organization**
2. Click **Leave Organization**

> **Note:** You must be part of another organization and cannot be the current owner. If you are the owner, [transfer ownership](/gk-dev/gk-dev-organization/#transfer-ownership) before leaving.

Leaving an organization will revoke your GitKraken license and access to shared collaboration features.

<figure>
  <img src='/wp-content/uploads/gk-dev-leave-organization.png' srcset='/wp-content/uploads/gk-dev-leave-organization@2x.png' class='img-bordered center help-center-img' alt='Leave organization screen in GitKraken'>
  <figcaption style='color:#888;text-align:center'>Leave your current GitKraken organization</figcaption>
</figure>

### Single sign-on

Single sign-on (SSO) is available for organizations that require it. For setup steps, visit the [Single Sign-On documentation](/gk-dev/gk-dev-single-sign-on/).


### Next Steps

- [Connect an Integration](/gk-dev/gk-dev-integrations/)
- [Learn how to manage your GitKraken subscription](/gk-dev/gk-dev-subscription/)
- [Return to GitKraken.dev Support Home](/gk-dev/gk-dev-home/)