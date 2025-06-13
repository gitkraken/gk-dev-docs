---
title: Security Controls & Cloud Patch Configuration
description: Learn how to manage GitKraken security settings, disable AI features, and configure self-hosted Cloud Patches via AWS S3.
taxonomy:
    category: gk-dev
---

<kbd>Last updated: June 2025</kbd>

GitKraken provides centralized security settings to help your organization control data-sharing features, enforce compliance, and manage where Git patches are stored.

***

## GitKraken AI Features

GitKraken AI features can suggest code or perform smart actions to improve your workflow. These features may require sending code snippets to GitKraken AI or third-party providers.

If these features don’t align with your organization's security policies, you can control access across your organization.

### Manage AI Feature Access

To enable or disable GitKraken AI features for all organization members:

- Go to **Settings > Security Controls > AI Features**
  - Requires [owner, admin, or billing contact](/gk-dev/gk-dev-organization/#roles)
  - Available on [Advanced+ plans](https://www.gitkraken.com/pricing)

<figure>
  <img src="/wp-content/uploads/administration-and-security-controls.png" srcset="/wp-content/uploads/administration-and-security-controls@2x.png" alt="GitKraken AI feature toggle in Security Controls">
  <figcaption style="color:#888;text-align:center">Organization-level toggle for GitKraken AI features</figcaption>
</figure>

### Enforce AI Providers

Organizations on the Business+ plans can enforce restrictions on which AI providers are allowed across GitKraken products. This ensures compliance with your data policies.

To configure provider-level controls:

1. Go to **Settings > Security Controls > Enforce AI providers**.
2. Enable the toggle to display supported providers.
3. For each provider, you can:
   - Enable: Allow team members to use the provider’s models.
   - Disable: Block the provider completely.

For the following marked* providers, you can also:
   - Set an API Key: Enforce the use of your key.
   - Add a Custom URL (requires a key): Restrict access to a specific endpoint.

Supported providers include:
- Anthropic*
- Azure*
- DeepSeek
- GitHub Copilot
- GitKraken AI
- Google*
- Hugging Face*
- Mistral*
- Ollama*
- OpenAI*
- OpenAI compatible*
- OpenRouter
- xAI

<figure>
  <img src="/wp-content/uploads/enforce-ai-providers.png" srcset="/wp-content/uploads/enforce-ai-providers@2x.png" alt="AI provider settings showing API key and URL fields">
  <figcaption style="color:#888;text-align:center">Example of AI provider configuration fields</figcaption>
</figure>

<div class='callout callout--info'>
  <p>
    Providers marked with an asterisk (*) support setting a custom API key and URL.
  </p>
  <p>
    These settings apply across all GitKraken products used by your organization.
  </p>
</div>

***

## Cloud Patches

Allow developers in your organization to create Cloud Patches that can be shared with others. Cloud Patches are encrypted Git patch files that GitKraken can store in GitKraken-managed or customer-managed storage.

If your company policies require internal storage, you can set up self-hosted Cloud Patches using your own AWS S3 bucket.

If this setup is not feasible, please contact our <a href="https://www.gitkraken.com/contact" target="_blank">customer success team</a>.

### Self-Host Cloud Patches with AWS S3

Configure your GitKraken organization to store Cloud Patches on your own infrastructure.

#### Requirements

- An AWS account with S3 access
- Admin permissions to apply bucket policies
- GitKraken Pro or Enterprise plan

#### Setup Steps

1. **Create an S3 bucket** and give it a meaningful name (e.g., `gitkraken-cloud-patches`).
2. **Apply the GitKraken-supplied bucket policy** using the UI template.
3. **Enter your AWS credentials** into GitKraken:
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

***

## Next Steps

- [Learn how to use Cloud Patches](/gk-dev/gk-dev-home/#cloud-patches-pro)
- [Manage Org Roles](/gk-dev/gk-dev-organization/#roles)
- [Explore GitKraken.dev Support Home](/gk-dev/gk-dev-home/)
