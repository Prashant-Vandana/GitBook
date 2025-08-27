---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in Microsoft SharePoint.
---

# Manage SharePoint Events

This document explains the impact on end-users and Microsoft SharePoint admins when the automated actions in SharePoint DLP are implemented.&#x20;

## Understanding SharePoint DLP Events

When an end user violates a policy in SharePoint DLP, an Event is generated based on the notification settings configured by you in the policy configurations. To learn more about Events, see [sdp\_events](../../../dashboard/sdp_events/ "mention").

To view the events specific to SharePoint, refer to [#understanding-exchange-dlp-events](../../../microsoft-exchange/exchange_online/policies/events.md#understanding-exchange-dlp-events "mention") section. (You can apply the SharePoint filter instead of the Exchange filter).

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../../dashboard/sdp_events/status.md "mention") document.

In SharePoint, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../../.gitbook/assets/image (1295).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The event detail view displays important information details about the file that triggered the event. You can find the details like the user whose actions triggered the event, the site ID, site name, library ID, library name to which the file belongs to, and so on.
{% endhint %}

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for SharePoint are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in SharePoint**: This option opens the file that triggered the event, in SharePoint.&#x20;
* **Download Original Content**: This action downloads a copy of the file that triggered the event.&#x20;
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the SharePoint,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to SharePoint,  through Slack.
* **Notify Teams**: This action notifies end user who added sensitive data file to SharePoint, through MS Teams.
* **Delete File Permanently**: This action deletes the file with sensitive data permanently from your SharePoint account.&#x20;
* **Move to Recycle Bin**: This action moves the file with sensitive data to the recycle bin.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user.
* **Restrict to Owner**: This action restricts the access of the file only to the file owner.&#x20;
* **Resolve**: This action must be taken when the sensitive data is removed completely. This action resolves the Event.



