---
title: Manage Your GitKraken Account
description: Set up and manage your GitKraken account used across GitKraken Desktop, GitLens, CLI, and more. Learn how to log in, personalize your profile, track your AI usage, and delete your account.
product: "GitKraken.dev"
content_type: "how-to"
audience: "all"
plan_required: "all"
status: "GA"
last_verified: "2026-04"
taxonomy:
    category: gk-dev
---

<kbd>Last updated: April 2026</kbd>

Your GitKraken account provides access to all GitKraken products and services, including GitKraken Desktop, GitLens, CLI, and GitKraken.dev. Use it to manage your identity, license, and preferences from a single dashboard. Creating a GitKraken account is free. Your license tier (Community, Pro, Advanced, Business, or Enterprise) is determined by your organization's subscription, not by the account itself.

<div class='callout callout--basic'>
  <p>Note that your GitKraken account is not compatible with <a href="/git-integration-for-jira-cloud/git-integration-for-jira-home-gij-cloud/">Git Integration for Jira</a>.</p>
  <p>We recommend using a single GitKraken account for yourself. Avoid creating duplicate accounts or sharing your account with others.</p>
</div>

***

## Quick Start

1. Go to [gitkraken.dev](https://gitkraken.dev?source=help_center) and select a login method: GitHub, GitLab, Bitbucket, Azure DevOps, Google, Microsoft, email, or SSO.
2. If using email, verify your address via the confirmation link sent to your inbox.
3. After signing in, click your avatar in the top right to access account settings: display name, avatar, licenses, email preferences, billing, and AI usage.
4. To update your avatar, navigate to account settings and follow the link to Gravatar. GitKraken uses Gravatar for profile images.
5. To review your weekly AI credit consumption, go to [gitkraken.dev/account#ai-usage](https://gitkraken.dev/account#ai-usage).
6. To delete your account, go to **Settings > Account Settings > Delete Account**. This action is GDPR-compliant and cannot be undone.

A single GitKraken account applies across all GitKraken products. Licenses are email-based and tied to one account per person. Avoid creating duplicate accounts.

***

## Sign in or create an account

Go to [gitkraken.dev](https://gitkraken.dev?source=help_center) and choose one of the supported login options:

| Login Method | Type | Notes |
|---|---|---|
| GitHub | Git provider | Also used for GitHub Student Developer Pack verification |
| GitLab | Git provider | |
| Bitbucket | Git provider | |
| Azure DevOps | Git provider | |
| Google | Identity provider | |
| Microsoft | Identity provider | |
| Email + password | Direct | Requires email verification via confirmation link |
| [SSO](/gk-dev/gk-dev-single-sign-on/) | Organization IdP | Available on Advanced or higher plans |

Each login method is tied to your primary email address. If you sign up with email, you’ll need to verify it via a confirmation link.

<figure>
  <img src="/wp-content/uploads/gk-dev-create-account-20260317.png" class="img-bordered center help-center-img" alt="GitKraken login options screen">
  <figcaption style="color:#888;text-align:center">Choose a connected service to authenticate with GitKraken</figcaption>
</figure>

***

## Personalize your account

Click your avatar in the top right to:

- Change your display name or avatar
- Manage your GitKraken licenses
- Configure email settings
- View your plan and billing information

<figure>
  <img src="/wp-content/uploads/gk-dev-account-personalization-20260317.png" class="img-bordered center help-center-img" alt="GitKraken account profile settings">
  <figcaption style="color:#888;text-align:center">Access account and license settings</figcaption>
</figure>

GitKraken uses [Gravatar](https://gravatar.com) to manage profile avatars. To change your avatar, select your profile image and follow the link to Gravatar. Updates may take several hours to appear.

***

## View your AI usage

Track how many AI credits you've consumed this week and which GitKraken AI features consumed them. Navigate to [gitkraken.dev/account#ai-usage](https://gitkraken.dev/account#ai-usage), or click your avatar and select **AI usage**.

The page shows usage for your account in the organization currently selected in GitKraken.dev. To view usage against a different organization, switch organizations using the top-left dropdown.

<figure>
  <img src="/wp-content/uploads/gk-dev-ai-usage-20260618.png" class="img-bordered center help-center-img" alt="AI usage page showing weekly credit total, shared weekly credits with a credit add-on, and a breakdown of credits consumed per AI feature">
  <figcaption style="color:#888;text-align:center">View your weekly AI credit consumption, shared credits and add-ons, and a per-feature breakdown</figcaption>
</figure>

The page is divided into three sections:

- **AI usage details** — Your personal weekly credit consumption (for example, `35.4k/4000k credits this week`). If you are approaching your limit, click **Upgrade your plan** to increase your allotment. If your organization needs more credits beyond its plan, additional credits can be purchased as credit add-ons. See [What are credit add-ons?](/gk-dev/gk-dev-ai-credits-faq/#what-are-credit-add-ons) in the AI Credits FAQ for details.
- **Organization usage** — Aggregate AI usage for the selected organization and the date the organization's allotment resets (shown in UTC).
- **Usage breakdown** — The GitKraken AI actions that have consumed credits this period (for example, **Commit Message** or **Explain Changes**), the share of total usage each represents, and — via the <kbd>?</kbd> tooltip — the exact token count consumed by that action. Click **See all AI actions** to view the full list.

<figure>
  <img src="/wp-content/uploads/gk-dev-ai-usage-breakdown-tooltip-20260424.png" class="img-bordered center help-center-img" alt="Tooltip on the Commit Message row showing the action description and token count">
  <figcaption style="color:#888;text-align:center">Hover the <kbd>?</kbd> icon next to an action to see its description and exact token count</figcaption>
</figure>

<div class='callout callout--info'>
  <p>AI credits are consumed based on the amount of content sent to the AI provider. Larger diffs, longer prompts, and repeated requests on the same input all increase token consumption. See <a href="/gk-dev/gk-dev-faq/#ive-consumed-all-my-weekly-tokens-in-1-commit-message-generation-why">the FAQ</a> for more detail.</p>
</div>

***

## Account settings vs. organization settings

Your GitKraken account and your GitKraken organization are managed separately:

- **Account settings** (name, avatar, email, login method) affect only your personal identity. Changes here do not affect other organization members.
- **Organization settings** (licenses, roles, SSO, teams, billing) affect all members of the organization. Only Owners, Admins, or Billing Contacts can change organization settings.

To manage your account, click your avatar in the top right. To manage your organization, select the organization from the top-left dropdown and navigate to **Settings**.

***

## Delete your account

To permanently delete your account:

1. Go to <strong>Settings > Account Settings</strong>
2. Click **Delete Account**
3. Confirm the deletion in the prompt

    > Note: If you are part of a GitKraken organization and not an admin, you’ll need an admin to remove your account before proceeding.

<div class='callout callout--warning'>
  <p>GitKraken is GDPR-compliant and this action cannot be undone. This action will revoke access to all GitKraken products and services linked to your account.</p>
</div>
