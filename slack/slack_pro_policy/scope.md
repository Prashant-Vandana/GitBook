---
description: >-
  Learn the process of configuring the Scope in the Slack Pro and Business+
  editions while creating a Nightfall policy.
---

# Configure Scope for Slack Pro and Slack Business+

This document explains how to set up the Policy Scope for Slack Pro and Slack Business+ editions. If you are using a Slack Enterprise edition, you must refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-2/scope).

The Scope stage allows you to select Slack Channels and Connections which must be scanned by the policy.&#x20;

To configure Policy Scope:

1. Select one of the following options under the **Select Channels** section. The scope of this policy is limited to only those channels and connections which you select in this section.&#x20;

* **Channels**: Select the **Select All** check box to scan the data in all your Slack channels. Select the **Public Channels** check box to scan data only in your Public Slack Channels. Select the **Private Channels** check box to scan data only in your private Slack channels.&#x20;
* **Connections**: Select the **Select All** check box to scan the data in all your Slack connections. Select the **Public Connect Channels** check box to scan data only in your Public connect Slack Channels. Select the **Private Connect Channels** check box to scan data only in your private connect Slack channels.

<figure><img src="../../.gitbook/assets/image (1226).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
You must add the Nightfall Pro Slack application to all the channels that you wish to scan with Nightfall.
{% endhint %}

## Applying Filters

The Filters section provides you an added level of granularity in setting the Scope. You can use specific filters to filter data based on Users, Groups, Channels, or Apps.&#x20;

## How Slack Filters Work

Slack policies support filtering based on users, user groups, and apps. These options provide flexible, granular control on whom to apply the monitoring. The **Only Include** option is very useful to pick specific required users, groups or apps for monitoring. particularly useful for creating broad policies with specific exceptions. Combining user and group options allows for complex, layered access control. The **exclude** option allows you to exclude the monitoring of unwanted users, user groups and apps, thus reducing the unwanted noise from secure entities.

<figure><img src="../../.gitbook/assets/image (1228).png" alt="" width="375"><figcaption></figcaption></figure>

### Filtering by Users

* **Only Include**: Only messages sent by selected users are scanned for sensitive data.&#x20;
* **Exclude**: Messages sent by excluded users are not scanned.&#x20;

### Filtering by Groups

* **Only Include**: Only messages sent by users in included Slack groups are scanned for sensitive data.&#x20;
* **Exclude**: Messages sent by users in excluded Slack groups are not scanned.

### Filtering by Apps

* **Only Include**: Only messages sent by included Slack apps are scanned for sensitive data.&#x20;
* **Exclude**: Messages sent by excluded Slack apps are not scanned.

## Priority Order for Conflict Management

Nightfall uses prioritization to decide which messages to scan when multiple filters are configured in a policy. The order of priority is:

1. User Exclusion
2. User Inclusion
3. Group Exclusion
4. Group Inclusion

**How it works:**

1\. Initially, Nightfall checks if the file owner is on the User Exclusion list. If they are, their messages are not scanned, no matter how other filters are configured in a policy.

2\. If the user isn't excluded, Nightfall then checks if they're on the User Inclusion list. If they are, all their messages are scanned for that policy.

3\. If the user isn't on either the exclusion or inclusion lists, Nightfall looks at group memberships. It checks if the user belongs to any excluded groups. If they do, their messages are not scanned for that policy.

4\. Finally, if none of the above apply, Nightfall checks if the user is in any included groups. If they are, their messages are scanned for that policy. If not, the messages are not scanned.

\
