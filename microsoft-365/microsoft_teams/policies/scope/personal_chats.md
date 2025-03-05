---
description: >-
  Learn how to configure the Scope section for personal chats in Microsoft Teams
  policy.
---

# Scope for Personal Chats

To monitor the chat messages between individual users, for sensitive data, you must first configure the Directory Sync feature for your Azure Entra account. This configuration gives Nightfall access to the list of users in your Azure account and thus Nightfall can monitor the messages sent between users.&#x20;

## Prerequisites to Monitor Chats

To monitor Chats, you must perform the following.

1. Configure the Directory Sync feature. Refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync/adding-microsoft-entra-id-to-nightfall).&#x20;
2. Once you complete the configuration, you must perform the steps mentioned in the [Monitoring Chats](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-microsoft-teams/configuring-policies/scope/scope-for-personal-chats#monitoring-chats) section of this document.

## Monitoring Chats

To Monitor Chat messages:

1. Enable the toggle switch, if not enabled.&#x20;

<figure><img src="../../../../.gitbook/assets/image (909).png" alt=""><figcaption></figcaption></figure>

2. Click **Add Tenant** and select the tenant to be monitored.&#x20;

<figure><img src="../../../../.gitbook/assets/image (910).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The **Add Tenant** button is displayed only if your organization has registered multiple M365 tenants with Nightfall. If your organization has registered a single M365 tenant, the tenant is selected by default and you will not see the **Add Tenant** butto&#x6E;**.**
{% endhint %}

{% hint style="info" %}
In the above image, you can see that the first two tenants are greyed out. This implies that the Directory Sync is not configured for these tenants. In such tenants, you can only monitor messages sent in groups and not messages sent between individual users.&#x20;
{% endhint %}

## Inclusion and Exclusions

### Inclusions

For the selected tenant, you must select the users that must be monitored. You can choose to monitor either all the users in the tenant or specific users or group of users.&#x20;

<figure><img src="../../../../.gitbook/assets/image (912).png" alt=""><figcaption></figcaption></figure>

When you select the **Specific user(s) & group(s)** option, two new drop-down menus are displayed. These menus allow you to select specific users or groups of users to be monitored.&#x20;

<figure><img src="../../../../.gitbook/assets/GIF Recording 2024-04-23 at 1.35.23 PM.gif" alt=""><figcaption></figcaption></figure>

### Exclusions

When you choose to monitor all the users, you may also choose a specific list of users or groups of users to exclude from monitoring. This is an optional configuration and you can skip it if you wish to monitor all the users.&#x20;

To exclude specific users and groups, select the users or groups in the exclusion section.&#x20;

<figure><img src="../../../../.gitbook/assets/GIF Recording 2024-04-23 at 1.42.13 PM.gif" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The Exclusion section is not applicable if you select the **Specific user(s) & group(s)** option in the Inclusion section.&#x20;
{% endhint %}

## Example Scenario

Acme Corp wishes to monitor the messages exchanged between all the users. They configure the Directory Sync for their MS Entra account and select the **All users** option in the inclusion section. However, they realize that there is an internal group in which users share dummy API keys, passwords, and credit card details, for testing. This group is called the **Test group**. To avoid false positive alerts, Acme Corp excludes the Test group from exclusion.&#x20;
