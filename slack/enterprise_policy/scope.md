---
description: >-
  Learn the process of configuring the Scope section while creating a Nightfall
  policy for the Slack Enterprise edition.
---

# Configure Scope for Slack Enterprise

This document explains how to set up the Policy Scope for the Slack Enterprise edition. If you are using a Slack Slack Pro or Slack Business+ editions, you must refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-1/scope).

The Scope stage allows you to select Slack Channels, Connections, and Direct Messages (DMs) which must be scanned by the policy.

{% hint style="info" %}
You must add the Nightfall Pro Slack application to all the channels that you wish to scan with Nightfall.
{% endhint %}

The Scope page allows you to set the Scope for one of the following entities.&#x20;

* **Workspaces:** Select the Workspaces radio button to configure the scope at the Workspace level. If you select the Workspace option, you can configure the Workspaces to be included in the scope. Within the Workspaces, you can choose to monitor specific types of Channels and Connections. Finally, you can also add filters to zero down on specific users, groups, channels, and apps.&#x20;
* **Specific Channel(s)**: Select the **Specific Channel(s)** radio button to monitor only specific Slack channels. Once you select the required Slack channels, you can add filters on the selected channels to monitor only specific users, groups, or apps.&#x20;

## Workspaces

In the Workspaces section, you must first select the Slack Workspaces to be monitored by the policy.&#x20;

<figure><img src="../../.gitbook/assets/image (1221).png" alt=""><figcaption></figcaption></figure>

### Select Channel Types and Connections

You can choose to monitor the following. You must select the check box for the channel type to be monitored.&#x20;

#### Channel Types

* **Public Channel**: Select this option to monitor all the messages sent by users in all the public Slack channels of the selected workspace(s).
* **Private Channel**: Select this option to monitor all the messages sent by users in all the private Slack channels of the selected workspace(s).
* **Direct Messages**: Select this option to monitor all the direct messages exchanged between users in the selected workspace(s).

#### Connections

* **Public Connect Channel**: Select this option to monitor all the messages sent by users in all the public Slack connect channels of the selected workspace(s).
* **Private Connect Channel**: Select this option to monitor all the messages sent by users in all the private Slack connect channels of the selected workspace(s).
* **Direct Messages**: Select this option to monitor all the direct messages exchanged between users in the selected workspace(s).

<figure><img src="../../.gitbook/assets/image (1222).png" alt=""><figcaption></figcaption></figure>

## Applying Filters

The Filters section provides you an added level of granularity in setting the Scope. You can use specific filters to filter data based on Users, Groups, or Apps.&#x20;

## How Slack Filters Work

Slack policies support filtering based on users, user groups, channels, and apps. These options provide flexible, granular control on whom to apply the monitoring. The **Only Include** option is very useful to pick specific required users, groups, channels or apps for monitoring. particularly useful for creating broad policies with specific exceptions. Combining user and group options allows for complex, layered access control. The **exclude** option allows you to exclude the monitoring of unwanted users, user groups, channels, and apps, thus reducing the unwanted noise from secure entities.

<figure><img src="../../.gitbook/assets/image (1223).png" alt="" width="375"><figcaption></figcaption></figure>

### Filtering by Users

* **Only Include**: Only messages sent by selected users are scanned for sensitive data.&#x20;
* **Exclude**: Messages sent by excluded users are not scanned.&#x20;

### Filtering by Groups

* **Only Include**: Only messages sent by users in included Slack groups are scanned for sensitive data.&#x20;
* **Exclude**: Messages sent by users in excluded Slack groups are not scanned.

### Filtering by Channels

* **Exclude**: Messages sent by users in excluded Slack Channels are not scanned. Enter the channel ID of the channel to be excluded.&#x20;

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

## Channels

To select specific channels to be scanned, you must first click the **Specific channel(s)** radio button. You must then enter the Slack channel ID of the channels that you wish to be scanned. To learn more about how to find the Channel ID of a Slack channel, see [#view-channel-id](scope.md#view-channel-id "mention").

<figure><img src="../../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure>

## View Channel ID

To view and copy the Channel ID of a Slack channel:

1. Click the required Slack Channel.
2. Click the **Get channel details** button.
3. Navigate to the bottom and click the **Copy channel id** button.

<figure><img src="../../.gitbook/assets/GIF Recording 2024-01-03 at 4.16.00 PM.gif" alt=""><figcaption></figcaption></figure>

## Applying Filters

The Filters section provides you an added level of granularity in setting the Scope. You can use specific filters to filter data based on Users, Groups, Channels, or Apps.&#x20;

## How Slack Filters Work

Slack policies support filtering based on users, user groups, and apps. These options provide flexible, granular control on whom to apply the monitoring. The **Only Include** option is very useful to pick specific required users, groups or apps for monitoring. particularly useful for creating broad policies with specific exceptions. Combining user and group options allows for complex, layered access control. The **exclude** option allows you to exclude the monitoring of unwanted users, user groups and apps, thus reducing the unwanted noise from secure entities.

<figure><img src="../../.gitbook/assets/image (1224).png" alt="" width="375"><figcaption></figcaption></figure>

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
