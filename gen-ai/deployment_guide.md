---
description: A deployment guide to manage GenAI apps through Nightfall browser plugin.
---

# Nightfall Browser Plugin Deployment Guide

## Introduction&#x20;

The Nightfall browser extension is a simple yet effective way to monitor usage of GenAI apps in your organization. This guide describes how to successfully deploy Nightfall DLP so that you can stop data sprawl, plug data leaks, and ensure continuous compliance. You will learn how to:&#x20;

1. Scan for any sensitive data (such as PII, PHI, PCI, credentials, or proprietary code) before submitting your prompt.&#x20;
2. Review AI-generated responses for any sensitive data that may come from third parties.
3. Evaluate AI-generated responses for accuracy, vulnerabilities, or malicious code before implementing them into your workflow.&#x20;

### Prerequisites

For a seamless deployment, we recommend having the following:

* Ability to manage browsers via the Google Admin console, a  Mobile device management (MDM) tool, or group policies&#x20;

To capture the full user context (who is using the GenAI app), the Nightfall browser extension requires each employee to log in. Today, the Nightfall browser extension supports these login flows:

* **Google SSO**: Google SSO is supported out of the box by Nightfall to log in to the GenAI extension. An auto-login is performed when the employee navigates to chat.open.ai and is currently logged into a Chrome profile associated with their work email.&#x20;
* **Azure Active Directory (AAD)**: Microsoft AAD is supported out of the box by Nightfall to log in to GenAI apps.
* **OIDC-Based SSO**: SAML SSO-based login requires additional configuration by Nightfall, based on your identity provider. Please contact support@nightfall.ai to enable SAML-based login to the ChatGPT extension. Additionally, you must have administrator access to the identity provider being used.

## Step 1: Set up the Nightfall Environment

**Reference the "How to" page** [**Create a Policy**](policies/) **(ChatGPT)**

1. Enable the integration by connecting with your Nightfall customer success manager or email [support@nightfall.ai](mailto:support@nightfall.ai)
2. Click the Policies tab on the left-sidebar
3. Select the + Add new policy and select ChatGPT
4. Follow the configuration steps to create a new policy
   * For testing, we recommend adding either the SSN, Credit Card or API Key detectors at Very Likely.

## Step 2: Install and test the Nightfall Browser DLP Extension

Reference “How To” page:[ ](https://help.nightfall.ai/nightfall-ai/nightfall-for-chatgpt/creating-policies-from-nightfall-console)[Install the Nightfall DLP for ChatGPT extension](https://help.nightfall.ai/nightfall-ai/nightfall-for-chatgpt/installing-nightfall-for-chatgpt)

**Google Chrome Marketplace**:

1. Open Google Chrome and on the top right, log in to your organization-managed Google Chrome profile (This is an optional step but will expedite the process).
2. Navigate to the[ Chrome marketplace listing](https://chrome.google.com/webstore/detail/nightfall-dlp-for-chatgpt/jgmgecncmjklkabkejnjfgfkglapfgek/related)
3. Click **+ Add to Chrome** and Add Extension.

**Firefox**&#x20;

1. Open the Firefox browser.
2. Navigate to [Firefox addons](https://addons.mozilla.org/en-US/firefox/).&#x20;
3. Click Add to **Firefox**.&#x20;

**GenAI app**:

1. Navigate to and log into any existing ChatGPT account, this can be a personal or work-associated account.
   * If you installed the Nightfall DLP browser plugin, proceed to log in to the Nightfall Chrome extension via Google or Microsoft SSO in order to continue using ChatGPT.
   * Once you log in to the Nightfall DLP browser plugin, the Nightfall logo is displayed at the bottom right corner of the screen (for ChatGPT, the logo appears in the field in which you enter the prompt.&#x20;
2. Enter in sample sensitive data, here is a Nightfall page of[ sample test data](https://playground.nightfall.ai/data)

{% hint style="info" %}
**Note**: The data should match the detection rules that were added in the policy
{% endhint %}

3. Validate that a Nightfall prompt appeared which highlighted the data in question
4. Continue submitting the redacted or original text to trigger a violation

**Nightfall:**

1. Click the **Violations** tab in the left-sidebar
2. Open the latest ChatGPT violation and inspect the findings

You have successfully installed and tested ChatGPT. Please continue testing the integration to ensure a smooth rollout process. Please see **Step 4** for more details on deployment methods and best practices.

## Step 3: Inform your organization about Nightfall DLP for GenAI apps

With the rollout of a new security tool, there requires a level of employee visibility and education. We have compiled a list of resources that can be used to inform your organization about Nightfall for GenAI app.

## Step 4: Rollout the Nightfall Browser extension to your organization

As a best practice, we recommended rolling the integration in a crawl, walk, run approach. Below is an ideal deployment timeline that was designed after working with a number of our customers.

**Ideal Deployment Timeline:**

* Week 1: Rollout to SecOps team for testing
* Week 2: Rollout to IT and InfoSec team for testing
* Week 3: Rollout to 50% of the company
* Week 4: Rollout to 75% of the company
* Week 5: Rollout to 100% of the company

**Deployment Methods:**

Since the browser extension requires complete coverage on all employee browsers, there are a few options for how this can be done. We recommend working with your IT admin and understanding which is the best way to roll out the extension given your company’s ecosystem.

* **Option 1**: Force install the extension to a subset of users via the Google admin console
  * [Google Admin Console](https://support.google.com/chrome/a/answer/6306504?hl=en)&#x20;
* **Option 2**: Use an MDM solution to rollout the extensions across your chromium browsers
  * [JAMF](https://learn.jamf.com/bundle/technical-paper-aws-verified-access/page/Downloading_and_Deploying_the_Manifest_File.html)&#x20;
  * [Kandji](https://support.kandji.io/support/solutions/articles/72000560463-google-chrome-management)&#x20;
  * [Chrome on Windows](https://support.google.com/chrome/a/answer/7532015?hl=en)&#x20;
  * [Edge on Windows ](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension)

**Option 3**: Require employees to manually install the extension to allow the usage of GenAI apps in your organization



\
