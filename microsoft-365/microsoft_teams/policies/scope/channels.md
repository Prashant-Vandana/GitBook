---
description: >-
  Learn how to configure the Scope section for personal chats in Microsoft Teams
  policy.
---

# Scope for MS Teams Channels

This document explains the process to configure the Scope section for messages sent in various groups of MS Teams.

To configure the Scope:&#x20;

1. Enable the toggle switch for **Teams**.&#x20;
2. Click **+ Add Tenant** and select the tenant.

<figure><img src="../../../../.gitbook/assets/image (913).png" alt=""><figcaption></figcaption></figure>

### Configuring the Inclusion Section

Once you select the tenant, you must select which Teams and Channels if the selected tenant, must be monitored by Nightfall. This selection can be done in the **Include in monitoring** section.

<figure><img src="../../../../.gitbook/assets/image (944).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
To learn more about Teams and Channels in MS Teams, you can refer to this [Microsoft documentation](https://support.microsoft.com/en-us/office/first-things-to-know-about-channels-in-microsoft-teams-8e7b8f6f-0f0d-41c2-9883-3dc0bd5d4cda).
{% endhint %}

#### Selecting Teams

1. Click the **All teams** radio button to monitor all the teams. This option monitors all the existing Teams present under the selected tenant. Additionally, any Team(s) created in the future will also be automatically included for monitoring.
2. (applicable only if you did not execute step 1) Click the **Specific team(s)** radio button to select the specific team(s) to be monitored.&#x20;

Once you select the **Specific team(s)** option, a new field **Teams** comes up. This field allows you to select the required teams by selecting the name of the team, as shown in the following image.

<figure><img src="../../../../.gitbook/assets/GIF Recording 2024-03-29 at 1.58.10 PM.gif" alt=""><figcaption></figcaption></figure>

The **Group of Teams** option allows you to select a set of Teams by entering a text string that may partially match a Team name. You can navigate to [this site](https://regex101.com/) to generate a regular expression pattern. The supported substring match operations are as follows.

* **Starts With**: Use this option to enter a text string which should match the start of a Team's name.
* **Ends With**: Use this option to enter a text string which should match the end of a Team's name.
* **Contains**: Use this option to enter a text string which should match a part of a Team's name.

<figure><img src="../../../../.gitbook/assets/image (945).png" alt=""><figcaption></figcaption></figure>

**Example Scenario for Patterns**

* Let's consider that some of the teams in your MS Teams tenant have external stakeholders too (people who are not part of your organization). A team with external stakeholders is named **ext-dev**, **ext-cs**, **ext-qa**, and so on.  To monitor all the external teams, you can use the **Starts with** option and use the substring **ext-.**
* Similarly, if you have ended all the team names that have external stakeholders, with the word **ext (dev-ext, qa-ext, cs-ext)**, you can select the **Ends With** option and enter the **-ext** substring. &#x20;
* Similarly, if you have used the word **ext** anywhere in the team name, you can select the **Contains** option and enter the substring **ext**.

#### Selecting Channels

Once you select the required teams, you must now select the channels of the selected team, to be monitored. Nightfall provides you with the following options to select the channel.&#x20;

* **Private Channels:** This option monitors all the private channels of the selected team(s).
* **Public Channels:** This option monitors all the public channels of the selected team(s).
* **Shared Channels:** This option monitors all the shared channels of the selected team(s).

<figure><img src="../../../../.gitbook/assets/image (946).png" alt=""><figcaption></figcaption></figure>

### Configuring the Exclusion Section&#x20;

The Exclusion section allows you to exclude certain channels from being monitored. You can enter a text string that should be present in the channel name that needs to be excluded.&#x20;

{% hint style="info" %}
This section is optional and you can skip it. You must configure this section only if you wish to exclude certain channels from being monitored.&#x20;
{% endhint %}

To use the exclusion section, click **Create a new Exclusion Rule** and select **Channel Exclusion**. You can navigate to [this site](https://regex101.com/) to generate a regular expression pattern.&#x20;

<figure><img src="../../../../.gitbook/assets/image (948).png" alt=""><figcaption></figcaption></figure>



* **Channel Exclusion**: This field allows you to enter a string that should be present in the Channel name for channels to be  excluded from being monitored. The various options are as follows.
  * **Starts With:** Use this option to enter a string that should be present at the start of the Channel name.
  * **Ends With:** Use this option to enter a string that should be present at the end of the Channel name.
  * **Contains:** Use this option to enter a string that should be present in the Channel name.

<figure><img src="../../../../.gitbook/assets/image (950).png" alt=""><figcaption></figcaption></figure>



#### Example Scenario

Consider that you wish to monitor all the channels in your MS Teams. However, there are a few test channels that were created internally just for testing and you wish to exclude these test channels. There are many test channels and test channels may also be created in the future. So, you need to manually add the newly created test channels as well in the exclusion list, which is cumbersome.

You can use the **Channel Exclusion** option, select the **Contains** option and enter the text string "**test**".
