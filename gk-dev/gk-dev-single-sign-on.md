---
title: Configure Single Sign-On (SSO) for GitKraken
description: Learn how to enable and configure Single Sign-On (SSO) using your identity provider (IdP) for secure access to GitKraken cloud organizations.
taxonomy:
    category: gk-dev
---

Single Sign-On (SSO) is an easy way to manage users across all your services. SSO is supported only for GitKraken cloud users; On-Premise plans are not supported.

Once your organization has set up SSO with an Identity Provider (IdP), the Owner or an Admin can link the GitKraken organization to that IdP. After linking, users associated with the IdP can log in to GitKraken apps and services.

<div class='callout callout--info'>
    <p>SSO is available with a GitKraken Advanced or Enterprise subscription. It’s also included in the 30-day multi-user trial.</p>
</div>

***

## What is single sign-on (SSO)?

<a href='https://en.wikipedia.org/wiki/Single_sign-on' target='_blank'>Single sign-on</a> (SSO) is an authentication method that lets users sign in once and gain access to multiple, independent software systems without needing to re-enter their credentials.

<figure>
  <img src="/wp-content/uploads/sso-example-diagram.png" class="img-bordered center help-center-img" alt="Diagram of a typical SSO setup">
  <figcaption style="color:#888;text-align:center">A typical SSO setup connecting users, identity providers, and apps</figcaption>
</figure>

Here are some important terms related to SSO:

**Directory Server:** A directory server stores information about organizational “objects” such as printers, computers, shared folders, users, or groups. These objects may be organized hierarchically.

Examples:
* <a href='https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/ad-ds-getting-started' target='_blank'>Microsoft Active Directory</a>
* <a href='https://www.oracle.com/security/identity-management/governance/' target='_blank'>Oracle Identity Governance (OIG) Suite</a>
* <a href='https://jumpcloud.com/' target='_blank'>JumpCloud</a>

**Identity Provider (IdP):** An IdP manages identity information and provides authentication services. It stores users, groups, and apps that rely on it to authenticate logins.

Examples:
* <a href='https://azure.microsoft.com/' target='_blank'>Azure Active Directory</a>
* <a href='https://www.okta.com/' target='_blank'>Okta</a>
* <a href='https://cloud.google.com/identity-platform' target='_blank'>Google Identity Platform</a>

Identity providers authenticate users on behalf of other apps, using a protocol called **OAuth**. This ensures the third-party apps can verify a user without needing access to their password.

**Third-party applications:** These are the services that use an IdP to authenticate users. Users are redirected to the IdP to log in, then returned to the application once verified.

Examples:
* <a href='https://www.gitkraken.com/' target='_blank'>GitKraken</a>
* <a href='https://slack.com/' target='_blank'>Slack</a>
* <a href='https://www.atlassian.com/software/jira' target='_blank'>Jira</a>

***

## How SSO works in GitKraken

GitKraken is a third-party application in this context. The Owner or an Admin of a GitKraken organization can set up SSO.

### Supported Identity Providers

GitKraken supports SAML 2.0 for SSO. Any identity provider (IdP) that supports SAML 2.0 is compatible.

### License Requirements

SSO requires a GitKraken Teams or Enterprise subscription, or a 30-day multi-user trial. To support multiple domains, GitKraken Enterprise or the multi-user trial is required.

### SSO Enforcement in GitKraken

- SSO is enforced at the **domain level**:
  - Users whose account emails match a verified SSO domain must log in via SSO.
  - Owners and Admins can log in using any method.

- SSO is also enforced at the **organization level**:
  - All users matching a verified domain must be part of the GitKraken organization.
  - Users with unmatched domains must be removed before SSO can be enabled.

- Additional rules:
  - Users cannot create other organizations or subscriptions.
  - Users cannot leave the organization or change their email/password.
  - Existing accounts with other organizations/subscriptions can keep them, but can’t access them until they are part of the organization and sign in with SSO.

### Just-in-time provisioning (JIT)

JIT can be enabled at <a href="https://gitkraken.dev/settings/sso?source=help_center&product=gitkraken_dot_dev">GitKraken.dev > Settings > SSO</a>. When JIT is active and a user logs in successfully via SSO, they will automatically join the organization and consume a license.

Note: JIT only works if there are available licenses. If none are available, users will not be added.

### SSO login experience

- On the login screen, select **SSO** to sign in.
- If a user tries to log in using a method other than SSO and matches a managed domain, they’ll see a message requiring SSO.
- If a user logs in with SSO but is not part of the organization, they’ll be prompted to contact an admin.
- Owners and Admins may sign in using any supported method.

<div class='callout callout--info'>
    <p>Gitkraken SSO does not support signing in through the Identity Provider's dashboard.</p>
</div>
***

## Set up SSO

1. Log in to <a href="https://gitkraken.dev?source=help_center&product=gitkraken_dot_dev">GitKraken.dev</a> as an Owner or Admin.
2. Navigate to **Settings > Single sign-on** in the left sidebar.
3. Click **Set up SSO**.
   - If existing connections appear, you may delete them to start from a blank state.
4. Complete the connection form:
   - **Connection name**: Name shown to users in GitKraken.
   - **Domain**: Use the base domain (e.g., gitkraken.com).
   - **Identity URL**: Provided by GitKraken, paste this into your IdP.
   - **Credentials**: Choose Metadata URL, raw Metadata, or Certificate. Paste in values from your IdP.
   - Click **Create Connection** when done.
5. Verify domain ownership:
   - Copy the TXT record provided.
   - Log in to your DNS provider and add the record.
   - Return to GitKraken and click **Verify Ownership**.
   - Note: DNS changes may take minutes or hours to propagate.
6. (Optional) Add additional domains:
   - If users span multiple domains, click **Add Connection** and repeat steps 4 and 5.
7. Enable SSO:
   - Ensure connections in the table are enabled (the presence of **Disable** means it is enabled).
   - Turn on the **Enable SSO** switch at the top.
   - You may be prompted to remove users with unmatched domains or to add external GitKraken users to your organization.
   - You may cancel and add more domains if needed.
   - (Optional) Enable JIT to allow new users to auto-join when signing in with SSO (requires available licenses).

SSO is now enabled and enforced across GitKraken for your domains. Be sure to test your setup. If you run into issues, contact GitKraken support.

*** 

## Example Identity Provider (IdP) setup instructions

<div class='callout callout--warning'>
    <p><strong>Note:</strong> These are example instructions to help you with Identity Provider setup. In most cases all you will need from us is the callback URL: https://api.gitkraken.com/oauth/sso/callback. If you need assistance please contact your IdP administrator or consult the IdP documentation for help.</p>
</div>

### G Suite

How to Create a SAML Application in G Suite:

1. Go to https://admin.google.com/ 
2. Click on <em>Apps</em> and then <em>Web and mobile apps</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-1.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Navigate to Web and mobile apps</figcaption>
</figure>
3. Click on <em>Add app</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-2.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Add a new application</figcaption>
</figure>
4. Click <em>Add custom SAML app</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-3.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Choose to add a custom SAML app</figcaption>
</figure>
5. Type in your app name (e.g., GitKraken SSO).
<figure>
  <img src="/wp-content/uploads/sso-example-idp-4.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Name your SAML app</figcaption>
</figure>
6. Copy your <em>SSO URL</em> and <em>Certificate</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-5.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Retrieve SSO URL and certificate</figcaption>
</figure>
7. Enter the callback URL <code>https://api.gitkraken.com/oauth/sso/callback</code> for both <em>ACS URL</em> and <em>Entity ID</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-6-1.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Input ACS URL and Entity ID</figcaption>
</figure>
8. Add desired attributes and click <em>Finish</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-7.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Configure attributes</figcaption>
</figure>
9. Click <em>TEST SAML LOGIN</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-8.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Test your SAML login</figcaption>
</figure>
10. Click <em>ALLOW ACCESS</em>.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-9.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Grant access to the app</figcaption>
</figure>
11. Select <em>ON for everyone</em> and save.
<figure>
  <img src="/wp-content/uploads/sso-example-idp-10.jpg" class="img-bordered center help-center-img">
  <figcaption style="color:#888;text-align:center">Enable the app for all users</figcaption>
</figure>

Now you are all set to <a href="/gk-dev/gk-dev-single-sign-on/#setup-sso">set up your SSO on a GitKraken Organization</a>.
- If a user tries to log in using a method other than SSO and matches a managed domain, they’ll see a message requiring SSO.
- If a user logs in with SSO but is not part of the organization, they’ll be prompted to contact an admin.
- Owners and Admins may sign in using any supported method.

### Azure Active Directory

How to create SAML application in Azure Active Directory:

1. In a browser, go to Azure login portal.
2. Enter your azure credentials and login.
3. Go to *Azure Active Directory* from search bar.
4. In the left menu click on *Enterprise applications*.

<img src="/wp-content/uploads/sso-azure-1.png" class="img-bordered help-center-img center">

5. Click on *New application* from the top of the page.

<img src="/wp-content/uploads/sso-azure-2.png" class="img-bordered help-center-img center">

6. Select *Create your own application*. 

<img src="/wp-content/uploads/sso-azure-3.png" class="img-bordered help-center-img center">

7. Give your application name (such as "GitKraken SSO") and select "Integrate any other application you don't find in the gallery (Non-gallery)".

<img src="/wp-content/uploads/sso-azure-4.png" class="img-bordered help-center-img center">

8. Select *Single sign-on* from the left sidebar and then choose *SAML*.

<img src="/wp-content/uploads/sso-azure-5.png" class="img-bordered help-center-img center">

9. Click the edit icon in the top right corner to configure SAML.

<img src="/wp-content/uploads/sso-azure-6.png" class="img-bordered help-center-img center">

10.  Input the *Entity ID* URI and *Reply URL*. Both of these should direct to `https://api.gitkraken.com/oauth/sso/callback` for GitKraken SSO. 

<img src="/wp-content/uploads/sso-azure-7-1.png" class="img-bordered help-center-img center">

Now you are all set to [setup your SSO on a GitKraken Organization](/gk-dev/gk-dev-single-sign-on/#setup-sso)
### Okta

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Logging through Okta Dashboard is not supported.</p>
</div>

How to Create SAML Application in Okta:

1. In a browser go to the Okta login page.
2. Enter your Okta credentials and login.
3. Go to admin dashboard and select *Applications* in navigation bar.

<img src="/wp-content/uploads/sso-okta-1.png" class="img-bordered help-center-img center">

4. Click on *Add Application*.  
5. Select *Create New App*. 

<img src="/wp-content/uploads/sso-okta-2.png" class="img-bordered help-center-img center">

6. Select *SAML 2.0* as a Sign on Method and click to next button.

<img src="/wp-content/uploads/sso-okta-3.png" class="img-bordered help-center-img center">

7. Enter a name of application (such as "GitKraken SSO").

<img src="/wp-content/uploads/sso-okta-4.png" class="img-bordered help-center-img center">

8. Configure SAML Integration. The *Single sign on URL* and *Audience URI* fields should direct to `https://api.gitkraken.com/oauth/sso/callback`.

<img src="/wp-content/uploads/sso-okta-5-1.png" class="img-bordered help-center-img center">

Step 9: Scroll down to the attribute statement and fill in the optional fields.

<img src="/wp-content/uploads/sso-okta-6.png" class="img-bordered help-center-img center">

Step 10: Select “I am an Okta customer adding an internal app” from option menu and then click to finish.

<img src="/wp-content/uploads/sso-okta-7.png" class="img-bordered help-center-img center">

Now you are all set to [setup your SSO on a GitKraken Organization](/gk-dev/gk-dev-single-sign-on/#setup-sso)

### Ping Identity

How to Create SAML Application in Ping Identity

1. Go to https://www.pingidentity.com/en/account/sign-on.html

2. Create an account or sign in your existing one.

3. Go to the home page and click on *Add Environment*.

<img src="/wp-content/uploads/sso-pingidentity-3.png" class="img-bordered help-center-img center">

4. Select the appropriate solution based on your need (in this guide, we use *Customer solution*) and click *Next*.

<img src="/wp-content/uploads/sso-pingidentity-4.png" class="img-bordered help-center-img center">

5.	Select *PingOne SSO*, then click *Next*.

<img src="/wp-content/uploads/sso-pingidentity-5.png" class="img-bordered help-center-img center">

6.	Type in your environment name (in *TRIAL ENVIRONMENT NAME*), then click *Finish*. Now your environment is created. Go ahead and click on it.

<img src="/wp-content/uploads/sso-pingidentity-6.png" class="img-bordered help-center-img center">
<img src="/wp-content/uploads/sso-pingidentity-6-2.png" class="img-bordered help-center-img center">

7.	Select Identities to add some users. Once you are done adding them click on Groups, and then click on the plus button to add a group. (Make sure to add users with their email addresses).

<img src="/wp-content/uploads/sso-pingidentity-7.png" class="img-bordered help-center-img center">
<img src="/wp-content/uploads/sso-pingidentity-7-2.png" class="img-bordered help-center-img center">

8.	Select *Groups*, then click on the plus button to add a group. Once you have that, you can add the users to your group.

<img src="/wp-content/uploads/sso-pingidentity-8.png" class="img-bordered help-center-img center">

9.	Select *Connections*.

<img src="/wp-content/uploads/sso-pingidentity-9.png" class="img-bordered help-center-img center">

10.	Click on the plus button.

<img src="/wp-content/uploads/sso-pingidentity-10.png" class="img-bordered help-center-img center">

11.	Enter a name for your application, then select *SAML Application*. Next click on the *Configure* button which appears once you select your application type.

<img src="/wp-content/uploads/sso-pingidentity-11.png" class="img-bordered help-center-img center">

12.	Select *Manually Enter*. Type in the URL for *ACS URLs* and *Entity ID*, then click on *Save*.
(URL: `https://api.gitkraken.com/oauth/sso/callback`)


<img src="/wp-content/uploads/sso-pingidentity-12.png" class="img-bordered help-center-img center">

13.	Click on the toggle button so the users would have access to your application.

<img src="/wp-content/uploads/sso-pingidentity-13.png" class="img-bordered help-center-img center">

14.	Click on *Attributes* then add email as your new attribute.

<img src="/wp-content/uploads/sso-pingidentity-14.png" class="img-bordered help-center-img center">
<img src="/wp-content/uploads/sso-pingidentity-14-2.png" class="img-bordered help-center-img center">

15. Time to add the group we created in Step 8.

<img src="/wp-content/uploads/sso-pingidentity-15.png" class="img-bordered help-center-img center">

16.	Select the pencil icon pictured below.

<img src="/wp-content/uploads/sso-pingidentity-16.png" class="img-bordered help-center-img center">

17.	Click on the plus icon to add the group, then click on *Save*.

<img src="/wp-content/uploads/sso-pingidentity-17.png" class="img-bordered help-center-img center">
<img src="/wp-content/uploads/sso-pingidentity-17-2.png" class="img-bordered help-center-img center">

18.	Go to the *Configuration* tab to copy your *IDP Metadata URL* and download your metadata (*Download Metadata* button).

<img src="/wp-content/uploads/sso-pingidentity-18.png" class="img-bordered help-center-img center">

19.	Log into <a href="https://gitkraken.dev/settings/sso?source=help_center&product=gitkraken_dot_dev">gitkraken.dev/settings/sso</a> and select "Setup SSO". Type in your Connection name and Domain. 

20.	Then use the *IDP Metadata URL* and *Metadata* from step 18 for *Metadata URL* and *Metadata*. Click on *Create Connection*

<img src="/wp-content/uploads/gkd-ping-identity-sso-connect-1.png" class="img-bordered help-center-img center">

21.	Now the users who were added in step 7 can *Sign in with SSO*.

