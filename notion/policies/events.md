---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in the Notion.
---

# Manage Notion Events

When an end user violates a policy in Notion, an Event is generated based on the notification settings configured by you in the policy configurations. To learn more about Events, see [sdp\_events](../../dashboard/sdp_events/ "mention").

This document explains where you can find notifications on policy violations and what actions can be taken.

## Nightfall Events

To view the Events in the Nightfall console:

1. Click **Detection and Response** from the left pane.
2. (Optional) Modify the days filter to view Events prior to last 7 days. By default the Events recorded in the **Last 7 Days** are displayed.

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

3. Apply filters to view only Notion Events.

<figure><img src="../../.gitbook/assets/image (1274).png" alt="" width="563"><figcaption></figcaption></figure>

Once you filter the Events to view only the Notion Events, you can refer to the [#event-list-view](../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../dashboard/sdp_events/status.md "mention") document.

In Notion, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

<figure><img src="../../.gitbook/assets/image (31).png" alt="" width="375"><figcaption></figcaption></figure>

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for Notion are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in Notion**: This action redirects to the sensitive data in the source Notion page. While this action is available only on the Event detail view, please note that relevant access to the source of sensitive data in Notion should be present.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through Slack.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user.
* **Redact**: This action redacts the sensitive data present in the Notion page.&#x20;
* **Remove Access**: This action removes the page from the web and/or removes guest access to the page.&#x20;
* **Delete Attachment**: This action deletes the sensitive data present in the attachments of a Notion page.
* **Resolve**: This action must be taken when the sensitive data is removed completely. This action resolves the Event.

{% hint style="info" %}
To learn more about how Nightfall handles Deduplication and Auto Resolution of Notion Events, see [#notion](../../dashboard/sdp_events/deduplication.md#notion "mention").
{% endhint %}



## Email Notification

* If you have configured Email Notification in [Admin Alerting](https://help.nightfall.ai/nightfall-ai/notion/configuring-policies/advanced-settings#admin-alerting), Nightfall admins receive the Email notification. This Email allows admins to take actions from within the Email.&#x20;
* If you have configured Email Notification in the Automation section of [End user notification](https://help.nightfall.ai/nightfall-ai/notion/configuring-policies/advanced-settings#end-user-notification) settings, end users receive an email from Nightfall. This Email allows end users to take actions from within the Email.&#x20;

<figure><img src="../../.gitbook/assets/GIF Recording 2023-11-19 at 3.31.09 PM.gif" alt=""><figcaption></figcaption></figure>

If you have selected Slack as an End-user remediation channel, end-users can perform the above tasks from Slack as well.&#x20;
