---
title: GitKraken Reseller Guide
description: Learn how to register, purchase, and manage GitKraken subscriptions as a reseller, including billing, payment methods, and subscription changes for customer organizations.
product: "GitKraken.dev"
content_type: "admin"
audience: "reseller"
plan_required: "Pro, Advanced, Business, Enterprise"
role_required: "Owner, Billing Contact, Reseller"
status: "GA"
last_verified: "2026-04"
taxonomy:
    category: gk-dev
---

<kbd>Last updated: April 2026</kbd>

This guide is for third-party resellers who purchase and manage GitKraken subscriptions on behalf of customer organizations. Resellers have a dedicated **Reseller** role that provides access to subscription management for the organizations they manage, including billing, payment methods, and plan changes. Available plans for reseller purchase include Pro, Advanced, Business, and Enterprise.

| Step | New Organization | Existing Organization |
|---|---|---|
| 1 | Create account with reseller email | Log in to existing account |
| 2 | Purchase subscription at [gitkraken.dev/purchase](https://gitkraken.dev/purchase) | Select customer org from dropdown |
| 3 | Add customer as Billing Contact | Go to Subscriptions > Edit Plan |
| 4 | Transfer ownership to customer | Increase seat count |
| 5 | Customer accepts activation link (7-day expiry) | Additional licenses are active immediately |

***

## Quick Start

To get started as a reseller:

1. Visit [gitkraken.dev/reseller](https://gitkraken.dev/reseller?source=help_center) and register or sign in using your reseller email address. Your account will automatically be associated with the customer organizations linked to your email.
2. Use the organization selector in the top-left to navigate to a customer organization.
3. Go to **Subscription** to manage billing, payment methods, and plan changes for that organization.

To purchase a new organization subscription, go to [gitkraken.dev/purchase](https://gitkraken.dev/purchase?source=help_center), set the seat count, enter the customer's organization name, and provide your payment details. After purchase, add the customer as a **Billing Contact** under **Users**, then transfer ownership under **Settings > Organization**. The customer receives an activation link valid for 7 days.

***

## How to register as a reseller

To access the reseller experience, visit [gitkraken.dev/reseller](https://gitkraken.dev/reseller?source=help_center). This takes you to a dedicated registration and sign-in flow for resellers.

1. **Register or sign in** using your reseller email address.
2. Your account will automatically be associated with the customer organizations linked to your email.
3. Once signed in, use the **organization selector** in the top-left to navigate between customer organizations.

<!-- TODO: Add screenshot of reseller registration flow once available -->

As a reseller, your view within each customer organization is simplified — you will only have access to the **Subscription** management page, where you can manage billing, payment methods, and plan changes.

<div class='callout callout--info'>
    <p>If your email is not yet associated with any customer organizations, <a href="https://www.gitkraken.com/sales-inquiries?source=help_center">contact our Customer Success team</a> to get set up.</p>
</div>

***

## How to purchase a new organization subscription

Follow this reseller guide for purchasing and user license management information.


### 1. Create an Account or Sign In

Go to [gitkraken.dev](https://gitkraken.dev/?source=help_center) and create a GitKraken account using your reseller email address.

- Use the email method (not social sign-in options).
- Do not input end-user details. Register using your own email.
- Verify your email address via the link sent to your inbox.

<div class='callout callout--basic'>
    <p>If you already use GitKraken for multiple customers, simply log in to your existing account and continue to Step 2.</p>
</div>

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-sign-in.png" srcset="/wp-content/uploads/gk-dev-reseller-sign-in@2x.png" class="help-center-img center img-bordered">
  <figcaption style="text-align: center; color: #888;">Sign in screen for resellers</figcaption>
</figure>

***

### 2. Purchase

Go to `Purchase Subscription`, choose the subscription type, set the number of seats, and enter payment details.

<div class='callout callout--basic'>
    <p>To create a new organization for a different customer, visit <a href="https://gitkraken.dev/purchase?source=help_center">gitkraken.dev/purchase</a>.</p>
</div>

- **Seats:** Number of licenses for the customer
- **Organization Name:** Name of the customer's organization
- **Payment Info:** Enter reseller billing information

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-purchase-0.png" srcset="/wp-content/uploads/gk-dev-reseller-purchase-0@2x.png" class="help-center-img center img-bordered">
  <figcaption style="text-align: center; color: #888;">Purchase subscription screen</figcaption>
</figure>

<div class='callout callout--basic'>
    <p>We accept card, PayPal, ACH, and Google Pay. Invoicing is available for large GitKraken Enterprise orders. Contact our <a href="https://www.gitkraken.com/sales-inquiries">Customer Success team</a> for invoicing support.</p>
</div>

After purchase, a receipt will be emailed to you.

***

### 3. Transfer Ownership to the Customer

Follow these steps to transfer the organization:

1. Go to [Users](https://gitkraken.dev/users?source=help_center)
2. Add the customer as a [Billing Contact](/gk-dev/gk-dev-organization/#roles)
3. Go to [Settings > Organization](https://gitkraken.dev/settings/organization?source=help_center) and transfer ownership

If the customer hasn’t verified their email, they’ll receive an activation link. They have 7 days to accept. If they miss the window, you can reinitiate the transfer.

***

## How to add licenses to an existing organization

Follow these steps to purchase additional licenses:

1. Log into [gitkraken.dev](https://gitkraken.dev/?source=help_center&product=gitkraken_dot_dev)
2. Select the customer’s organization from the top-left dropdown
3. Go to the "Subscriptions" tab
4. Update billing info if needed
5. Click "Edit Plan"
6. Increase the total user count
7. Review the Billing Summary for cost. You can also click "View Prorated Charges Quote" to generate a formal quote document for the additional licenses.
8. Click “Save.” The additional licenses will be active immediately.

<div class='callout callout--basic'>
    <p>License costs are prorated against the original billing cycle. If a customer org is not listed under your account, <a href="https://www.gitkraken.com/sales-inquiries?source=help_center">contact our Customer Success team</a>.</p>
</div>

***

## Reseller subscription management

When you navigate to a customer organization as a reseller, the **Subscription** page provides access to manage billing information, payment methods, and subscription changes. Billing and payment method updates apply to your reseller account and are shared across the organizations you manage. Subscription changes (such as plan tier or seat count) apply to the specific customer organization and are billed to your reseller account.

### Update billing information

From the Subscription page, click **Update** next to your billing information to update your billing address. Changes to billing information apply to your reseller account.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-update-billing-info.png" class="img-bordered center help-center-img" alt="Update billing information form for resellers" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Update your billing address from the Subscription page.</figcaption>
</figure>

### Update payment method

Click **Update** next to your payment method to change the card or payment method on file for your reseller account.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-update-payment-method.png" class="img-bordered center help-center-img" alt="Update payment method dialog for resellers" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Update the payment method linked to your reseller account.</figcaption>
</figure>

### Delete payment method

If you need to remove a payment method, click **Delete** next to the payment method. A confirmation dialog will appear. This action cannot be undone and may affect your subscription.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-delete-payment-method.png" class="img-bordered center help-center-img" alt="Delete payment method confirmation dialog" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Confirm before deleting a payment method.</figcaption>
</figure>

### Edit subscription

Click **Edit Plan** to change the plan tier or adjust the number of seats for the customer organization. The Edit Plan page shows a **Renewal preview** with the updated cost. From this page you can also update or delete the payment method on file.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-edit-plan.png" class="img-bordered center help-center-img" alt="Edit Plan page as seen by a reseller" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Resellers can change plans, adjust seats, and manage payment methods from the Edit Plan page.</figcaption>
</figure>

Click **Save** to apply the changes, or use **Create quote** to generate a formal quote before committing. See [How to create a quote](/gk-dev/gk-dev-subscription/#create-quote) for details.

***

## What organization members see

When an organization is managed by a reseller, members with the Owner, Admin, or Billing Contact role will see a simplified Subscription page. Billing information, payment methods, and subscription changes are not available to organization members — these are managed exclusively by the reseller.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-restricted-subscription.png" class="img-bordered center help-center-img" alt="Restricted subscription view for organization members" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Organization members see a read-only subscription page when the organization is managed by a reseller.</figcaption>
</figure>

Actions that would result in a charge — such as adding members beyond the subscription seat count — are also restricted. Organization members will see a message indicating that the organization is managed by a reseller and that only the reseller can perform that action.

<figure>
  <img src="/wp-content/uploads/gk-dev-reseller-restricted-add-users.png" class="img-bordered center help-center-img" alt="Add Users dialog showing restriction for reseller-managed organizations" style="display: block; margin: 0 auto;">
  <figcaption style="color: #888; text-align: center;">Adding users beyond the seat count is restricted when the organization is managed by a reseller.</figcaption>
</figure>

***

## How to generate quotes

You can generate formal quotes for renewals and mid-cycle upgrades (such as adding seats or changing plans) directly from the Edit Plan page. See [How to create a quote](/gk-dev/gk-dev-subscription/#create-quote) for step-by-step instructions.
