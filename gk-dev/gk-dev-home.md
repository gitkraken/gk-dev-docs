---

title: gitkraken.dev
description: Learn how to work with gitkraken.dev
taxonomy:
    category: gk-dev

---

GitKraken.dev offers many of the GitKraken developer collaboration tools all within a browser via desktop or mobile. In addition, it allows you to manage Security Controls for users within your [GitKraken Organization](/gitkraken-client/gitkraken-organization/). 

<img src="/wp-content/uploads/gkd-main.png" class="img-responsive center img-bordered"> 

***

## Focus View

The Focus View will provide you with a summary of pull requests and issues relevant to you for the filtered selection as well as allow you to take action on these items. Instead of hunting for these pieces of information separately, you can get a holistic view of what you’re working on.

<img src="/wp-content/uploads/gkd-focus-view.png" class="img-responsive center img-bordered"> 

There is a search bar and filters to limit the issues and pull requests shown. Actions can be taken on issues and pull requests from the Actions column. Both can be opened on the connected service by selecting `Open`. Additionally, from the `Open` dropdown, pull requests can be opened in GitKraken Client, VS Code, and VS Code Insiders. 

Items in the Focus View can be pinned, to move the item to the top of the list, and can be snoozed, to be hidden under the SNOOZED section. To pin or unpin and item, click the pin <i class="fa-solid fa-thumbtack"></i> in the pin column. To snooze an item, hover over an item, select the snooze <i class="fa-solid fa-snooze"></i> icon, and select the desired time option - selecting snooze will snooze the item until it is manually unsnoozed. To unsnooze an item, click on the `SNOOZED` section header, hover over the desired item and select the unsnooze icon for that item.

<img src="/wp-content/uploads/gkd-pin-or-snooze.gif" class="img-responsive center img-bordered"> 

***

## Integrations

To begin working with the Focus View, start by connecting an integration from https://gitkraken.dev/settings/integrations. To connect an integration, select the desired integration.

- For Cloud integrations: Log in to the desired account and then approve access for GitKraken.
- For Self-Hosted/Server integrations: Fill out Host Domain, select `Generate a token on {service}` - this will open the service on the PAT creation page with the required scopes, fill out the PAT and then select `Connect`.

<img src="/wp-content/uploads/gkd-integrations.png" class="img-responsive center img-bordered"> 

<div class='callout callout--basic'>
   	<p>Note for GitHub.com: In order to work with repositories owned by a GitHub organization, the organization will need to allow <a href="https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/">Organization Approval</a> for GitKraken.</p>
</div>

***

## Administration & Security Controls

Enable, disable, or configure features for users in your organization. 

<img src="/wp-content/uploads/gkd-security-controls.png" class="img-responsive center img-bordered"> 

### AI features

The GitKraken suite includes a lineup of AI features that are intended to speed up your workflow. These features require sending some of your code to an AI hosted on the cloud such as ChatGPT. If you are concerned that AI features do not comply with your company’s data security, you can disable AI features for everyone in your organization. Please note that changing this setting requires you to have the role [owner, admin, or billing contact](/gitkraken-client/gitkraken-organization/#roles) on a [Teams or Enterprise plan](https://www.gitkraken.com/pricing).


### Cloud Patches

Allow developers in your organization to create Cloud Patches that can be shared with others. A Cloud Patch is a Git patch that is stored securely by GitKraken. If you are concerned that Cloud Patches do not comply with your company’s data security, you can set up self-hosted Cloud Patches for your organization. If this is not an option for you, please [contact our customer success team](https://www.gitkraken.com/sales-inquiries).

#### Self-hosted

You can host your organization’s Cloud Patches on your own AWS S3 bucket. To do so login to https://gitkraken.dev/settings/security, copy the bucket policy by clicking “Copy policy.” Open the AWS Console and navigate to the S3 service. From there, click on the bucket you want to store Cloud Patches. Click the "Permissions" tab and look for the “Bucket policy" section. Click the "Edit" button and paste the bucket policy into the text box. Rename CUSTOMER_BUCKET_NAME with the name of your bucket. Finally, click "Save changes” and return to https://gitkraken.dev/settings/security to test your bucket.

Please note to setup self-hosted Cloud Patches require you to have the role [owner, admin, or billing contact](/gitkraken-client/gitkraken-organization/#roles) on an [Enterprise plan](https://www.gitkraken.com/pricing).

<img src="/wp-content/uploads/gkd-self-hosted-bucket.png" class="img-responsive center img-bordered"> 