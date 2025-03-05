---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in the Microsoft OneDrive.
---

# Manage OneDrive Events

When Nightfall detects a violation to one or more OneDrive SDP policies, it reports the violation as an Event. This document describes workflows and options for the OneDrive Events. Furthermore, it is recommended to read the Nightfall Events [sdp\_events](../../../dashboard/sdp_events/ "mention") document before proceeding further.

## Nightfall Events

To view the Events on the Nightfall console:

1. Click **Detection and Response** from the left pane.
2. Filter the data to view only the OneDrive Events.&#x20;

<figure><img src="../../../.gitbook/assets/image (1265).png" alt="" width="563"><figcaption></figcaption></figure>

3. (Optional) To view Events prior to the **Last 7 days**, click on the date filter and choose the appropriate date range or enter a custom date range.

<figure><img src="../../../.gitbook/assets/image (1244).png" alt=""><figcaption></figcaption></figure>

Once you filter the Events to view only the OneDrive events, you can refer to the [#event-list-view](../../../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

<figure><img src="../../../.gitbook/assets/image (1245).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../../../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../../../dashboard/sdp_events/status.md "mention") document.

In OneDrive, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../../../.gitbook/assets/image (1251).png" alt="" width="563"><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.&#x20;

<figure><img src="../../../.gitbook/assets/image (1252).png" alt="" width="375"><figcaption></figcaption></figure>

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../../../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for OneDrive are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in OneDrive**: This action redirects to the relevant document with sensitive data in the source OneDrive. While this action is available only on the Event detail view, please note that relevant access to the document in source OneDrive should be present.
* **Download Original Content**: This action downloads the original file that contains sensitive data. If the file is deleted or moved to a different location within OneDrive, this action fails. This action is available only on the Event detail view.
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through email.
* **Notify Slack**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through Slack.
* **Notify Teams**: This action notifies the end user who added the sensitive data file to the OneDrive about the event,  through MS Teams.
* **Delete File**: This action deletes the file containing sensitive data, from OneDrive.&#x20;
* **Move to Recycle bin**: This action moves the file containing sensitive data, to the OneDrive recycle bin.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user
* **Restrict to Owner**: This action restricts the access of the file containing the sensitive data to only the owner of the file.&#x20;
* **Resolve**: This action must be taken when the sensitive data is removed completely from the source file. This action resolves the Event.&#x20;

{% hint style="info" %}
To learn more about how Nightfall handles Deduplication and Auto Resolution of OneDrive Events, see [#onedrive](../../../dashboard/sdp_events/deduplication.md#onedrive "mention").
{% endhint %}



## Email Notifications

* If you have configured Email Notification in [Admin Alerting](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-onedrive/onedrive-policies/advanced-settings#admin-alerting), Nightfall admins receive the Email notification. This Email allows admins to take actions from within the Email.&#x20;
* If you have configured Email Notification in the Automation section of [End user notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-onedrive/onedrive-policies/advanced-settings#end-user-notification)[ ](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification)settings, end users receive an email from Nightfall. This notification allows end users to take remedial actions from within the Email. The available remedial actions depend on the settings configured in the [end user remediation](https://help.nightfall.ai/nightfall-ai/nightfall-for-microsoft-365/nightfall-for-onedrive/onedrive-policies/advanced-settings#end-user-remediation) section.



