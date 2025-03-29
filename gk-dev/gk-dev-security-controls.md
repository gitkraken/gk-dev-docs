---

title: Security Controls
description: Learn how to work with security controls on gitkraken.dev
taxonomy:
    category: gk-dev

---

Manage security controls for your organization and users.

***

## Gitkraken AI features

The GitKraken suite includes Gitkraken AI features that are intended to speed up your workflow. These features require sending some of your code to Gitkraken AI hosted on the cloud. If you are concerned that AI features do not comply with your company’s data security, you can disable AI features for everyone in your organization. Please note that changing this setting requires you to have the role [owner, admin, or billing contact](gk-dev/gk-dev-organization/#roles) on a [Teams or Enterprise plan](https://www.gitkraken.com/pricing).

***

## Cloud Patches `PRO`

Allow developers in your organization to create Cloud Patches that can be shared with others. A Cloud Patch is a Git patch that is stored securely by GitKraken. If you are concerned that Cloud Patches do not comply with your company’s data security, you can set up self-hosted Cloud Patches for your organization. If this is not an option for you, please [contact our customer success team](https://www.gitkraken.com/sales-inquiries).

### Self-hosted

You can host your organization’s Cloud Patches on your own AWS S3 bucket. To do so login to https://gitkraken.dev/settings/security, copy the bucket policy by clicking “Copy policy.” Open the AWS Console and navigate to the S3 service. From there, click on the bucket you want to store Cloud Patches. Click the "Permissions" tab and look for the “Bucket policy" section. Click the "Edit" button and paste the bucket policy into the text box. Rename CUSTOMER_BUCKET_NAME with the name of your bucket. Finally, click "Save changes” and return to https://gitkraken.dev/settings/security to test your bucket.

Please note to setup self-hosted Cloud Patches require you to have the role [owner, admin, or billing contact](gk-dev/gk-dev-organization/#roles) on an [Enterprise plan](https://www.gitkraken.com/pricing).

<img src="/wp-content/uploads/gkd-self-hosted-bucket.png" class="img-responsive center img-bordered"> 
