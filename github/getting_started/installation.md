---
description: Learn how to install Nightfall DLP for GitHub.
---

# Install Nightfall for GitHub

You can install Nightfall for GitHub via the [Nightfall console](installation.md#installing-nightfall-for-github-from-nightfall-console). The Nightfall app for GitHub requires the following permissions:

* **Read** access to code, commit statuses, and metadata
* **Read** and **write** access to issues and pull requests
  * Nightfall has an option to notify developers for violations via email. Further, the Nightfall app for GitHub also needs read and write permissions on issues and pull requests to tag developers in pull request comments. These permissions are needed by Nightfall to tag developers for violations in a commit or a Pull Request.&#x20;

## Installing Nightfall for GitHub from Nightfall console

To install from Nightfall's console,

1. Go to Nightfall's dashboard [here](https://app.nightfall.ai/dashboard).
2. Click **GitHub** under **My Integrations**. The GitHub Account Information screen displays. If GitHub is not listed under My Integrations but is in Available Integrations, please reach out to your Nightfall contact.&#x20;
3. Click **+ Add Org**. The GitHub sign-in page displays.
4. Log in to the GitHub instance where you wish to install Nightfall for GitHub. If you are already logged in to your GitHub account, you only need to enter the password.

{% hint style="info" %}
If you have enabled multi-factor authentication (MFA) on your GitHub account, you receive an authorization code. You must enter this code to continue the installation process.
{% endhint %}



<div data-full-width="true"><figure><img src="../../.gitbook/assets/GIF Recording 2023-10-30 at 3.24.25 PM.gif" alt=""><figcaption></figcaption></figure></div>

5. Ensure that the **All repositories** radio button is selected on the Authorization page. This ensures that all of your GitHub repositories are monitored by Nightfall. Nightfall recommends you to select this option. To monitor only a specific set of repositories, select Only select repositories radio button and select the required repositories.
6. Click **Install and Authorize**.

![](<../../.gitbook/assets/Screenshot 2023-10-30 at 3.25.48 PM.png>)

{% hint style="info" %}
If you select only some specific repositories to be monitored by Nightfall and later on wish to monitor more repositories or all the repositories, refer to [this section.](installation.md#add-multiple-repositories)&#x20;
{% endhint %}

Nightfall for GitHub is now successfully installed. You can check your GitHub username under the Account Information section of the GitHub integration.&#x20;

## Modify Repository Settings

This section explains how you can modify the repository settings configured while installing Nightfall for GitHub. This section helps you in the following scenarios.

* While installing Nightfall for GitHub, you have allowed only a few repositories to be monitored by Nightfall, and now wish that Nightfall monitors more or all of your GitHub repositories.
* While installing Nightfall for GitHub, you have allowed all your GitHub repositories to be monitored by Nightfall and now wish only a few repositories to be monitored.

To modify Repository settings:

1. Log in to the GitHub account on which Nightfall for GitHub is installed.&#x20;
2. Click the name icon on the extreme right corner and select Settings.
3. Select **Applications** under the I**ntegrations** section from the left menu.
4. Select **Configure** for the Nightfall for the GitHub application.&#x20;

<div data-full-width="true"><figure><img src="../../.gitbook/assets/GIF Recording 2023-10-30 at 3.54.22 PM.gif" alt=""><figcaption></figcaption></figure></div>

5. Scroll down to the **Repository access** section and make the necessary changes.&#x20;
6. Click **Save**.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-10-30 at 3.56.24 PM.gif" alt=""><figcaption></figcaption></figure>

##



