---
description: Learn how to install Nightfall DLP for Salesforce.
---

# Install Nightfall DLP for Salesforce

## Requirements

Registering a Salesforce organization involves two steps:

1. Deploying the Nightfall DLP package to the Salesforce organization
2. Authorising the Nightfall DLP package to be used to scan updates to Salesforce

To successfully execute the above two steps, the credentials of a Salesforce user with a System Admin profile would be required.

* Nightfall can ‘auto-discover' all Sandbox organizations associated with a production organization. Upon installing Nightfall in a production organization, the system administrator grants privileges to the organization using OAuth, Nightfall displays all sandbox organizations within the organization.&#x20;

All sandbox organizations display as **Unauthorized** until the administrator explicitly sets up these organizations for scanning by Nightfall.

* The user account must remain valid and set up as a Salesforce admin profile while the Salesforce org is onboarded and remains active on Nightfall.
* Credentials for a user account that is of type Salesforce admin profile

The user account should remain valid and set up as a Salesforce admin profile while the Salesforce org is onboard and remains active on Nightfall.

## Installation

1. Click **Salesforce** under the Integrations section, from the left menu bar.&#x20;
2. Click **Begin Setup** on the **Salesforce Setup** section.&#x20;
3. Select one of the Salesforce org types.
   * **Sandbox**: Select this option to install the Nightfall DLP for Salesforce in a sandbox environment. &#x20;
   * **Production**: Select this option to install the Nightfall DLP for Salesforce in an actual Salesforce production environment.
4. Click **Install**. The Salesforce login page is displayed in a new browser tab.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-Mg3wgFIu8T7XAT1u-f_%2Fuploads%2FvawNXhDTXKv4xXdfVRaC%2FGIF%20Recording%202023-12-18%20at%205.24.52%20PM.gif?alt=media&#x26;token=9190b810-1c37-455d-b974-3390a1db0ca8" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
**IMPORTANT**

If you have enabled SSO on your Salesforce account, Nightfall does not redirect you to the SSO page in Salesforce when you click the **Install** button in the previous step. You are still redirected to the Salesforce login page. In this case, you must perform one of the following tasks.

* On the Salesforce login page, click the **Use Custom** **Domain** button. You are redirected to Salesforce Custom Domain page. On the Custom Domain page, you must enter your organisation's salesforce domain and hit the enter key. If you have set up redirection on your Salesforce domain, you are redirected to the SSO page and you must login with SSO and the installation process continues.

&#x20;                                                                                 OR

* If you have not set up redirection on your Salesforce domain, you must first login to your Salesforce account using SSO and then navigate to the Nightfall UI and start the installation process. In this case, you need not enter the credentials after clicking the **Install** button and the process will continue without any bottlenecks.
{% endhint %}

The Salesforce **Installed Packages** window is displayed. Verify that the Nightfall DLP package is displayed.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-Mg3wgFIu8T7XAT1u-f_%2Fuploads%2FV8LSuZAQwnyDagxuUvwj%2FGIF%20Recording%202023-12-18%20at%205.42.47%20PM.gif?alt=media&#x26;token=45835eac-5ad7-47b5-a3d9-fc7f3ca125ef" alt=""><figcaption></figcaption></figure>

9. Return to the browser in which you opened the Nightfall App. The **Authenticate with Salesforce** window is displayed.&#x20;
10. Click **Authenticate**. The Salesforce permission page is displayed.&#x20;
11. If a permission link is displayed, click **Allow**.&#x20;
12. Click **Finish**.

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F-Mg3wgFIu8T7XAT1u-f_%2Fuploads%2FqECVTQa3oPl1sCwjAzCF%2FSalesforce%20authentication.gif?alt=media&#x26;token=f0751667-ccc8-4b18-8ab5-e0fc84198f44" alt=""><figcaption></figcaption></figure>
