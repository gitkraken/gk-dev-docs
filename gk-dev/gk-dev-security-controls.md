---
title: Security Controls
description: Learn how to manage security settings and configure a private AWS S3 bucket for Cloud Patches.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

GitKraken offers built-in security settings and options to manage both AI features and Cloud Patches for your organization.

***

## GitKraken AI features

GitKraken AI features can help speed up your workflow by suggesting code or performing smart actions. These features may require sending code snippets to GitKraken AI hosted in the cloud.

If these features do not align with your organization's data policies, you can disable GitKraken AI for all users in your organization from <strong>Settings > Security Controls</strong>.

Disabling AI features requires you to have the role of [owner, admin, or billing contact](/gk-dev/gk-dev-organization/#roles) on a [Teams or Enterprise plan](https://www.gitkraken.com/pricing).

***

## Cloud Patches
Allow developers in your organization to create Cloud Patches that can be shared with others. 

If you are concerned that Cloud Patches do not comply with your company’s data security, you can set up self-hosted Cloud Patches for your organization. If this is not an option for you, please contact our <a href="https://www.gitkraken.com/contact" target="_blank">customer success team</a>.

### Self-host Cloud Patches

Cloud Patches are encrypted Git patch files that can be stored on your own AWS S3 bucket instead of GitKraken-managed storage.

#### Requirements

Setting up self-hosted Cloud Patches requires the following:

- An AWS account with access to S3
- Administrator role permissions to configure a bucket policy
- GitKraken Pro or Enterprise plan

#### Step-by-step setup

1. **Create an S3 bucket** in AWS and name it something meaningful (e.g., `gitkraken-cloud-patches`).
2. **Apply the correct bucket policy** using the template provided in the GitKraken UI.
3. **Add credentials** to GitKraken by providing:
    - Bucket name
    - Access key ID
    - Secret access key
    - AWS region
4. **Test the connection** and save your configuration.

<figure>
  <img src="/wp-content/uploads/gkd-self-hosted-bucket.png" class="img-bordered center help-center-img" alt="AWS S3 bucket permissions configuration">
  <figcaption style="color:#888;text-align:center">AWS S3 permissions screen for GitKraken Cloud Patches</figcaption>
</figure>

<div class='callout callout--warning'>
  <p>
    GitKraken encrypts all Cloud Patches, even when self-hosted. Only users with access to the patch link and repository permissions can view contents.
  </p>
</div>
