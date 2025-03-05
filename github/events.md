---
description: >-
  Learn how to handle Nightfall Events that were created as a result of
  sensitive data leak in GitHub.
---

# Manage GitHub Events

When an end user violates a policy in GitHub, Events are generated in GitHub and you can view these Violations on the [Nightfall Event](https://help.nightfall.ai/sensitive-data-protection/dashboards_violations/nightfall-events) console.&#x20;

GitHub integration implements [Deduplication](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations#filtering-duplicates) across GitHub Events. Deduplication reduces the number of distinct Events created for a finding that is already accounted for by an active Event related to the same GitHub branch.

The following table summarises the treatment of a GitHub Event with Deduplication in action when the developer(s) push changes to a file in a GitHub branch.

<table><thead><tr><th width="257">State of existing Nightfall Violation</th><th width="222">Developer Action on a file in GitHub repo</th><th>Automated actions due to Deduplication</th></tr></thead><tbody><tr><td>No existing Event</td><td>Introduce sensitive data</td><td>New Event Created</td></tr><tr><td>Active Event not in a resolved state</td><td>Additional code with sensitive data pushed</td><td><ol><li>Increment finding(s) in the existing Event</li><li>Create an Event with all the new findings</li></ol></td></tr><tr><td>Active Event not in a resolved state</td><td>Code with sensitive findings redacted</td><td><ol><li>Number of findings in the existing Event updated</li><li>If no finding remaining then the Event is marked resolved</li></ol></td></tr><tr><td>Event is in a resolved state</td><td>Additional code with sensitive data pushed</td><td>New Event created</td></tr></tbody></table>



The following table summarises the treatment of a GitHub violation with Deduplication in action when the developer(s) clones/merges a GitHub branch.

| State of existing Nightfall Event    | Developer Action on a file in GitHub repo        | Automated actions due to Deduplication                                                        |
| ------------------------------------ | ------------------------------------------------ | --------------------------------------------------------------------------------------------- |
| No existing Event                    | Branch Clone                                     | No new Events                                                                                 |
| Active Event not in a resolved state | Branch Clone                                     | <ol><li>No new Events in the original branch</li><li>No Events in the cloned branch</li></ol> |
| No existing Event                    | Merge Cloned Branch back or Delete Cloned Branch | No new Events                                                                                 |
| No existing Event                    | Merge Cloned Branch back or Delete Cloned Branch | <ol><li>No new Events</li><li>Existing Events from the Cloned Branch resolved</li></ol>       |

When an Event is automatically resolved by the GitHub Deduplication feature (as a result of sensitive data being removed from the concerned GitHub file/repo) the log section of the Event displays a **Resolved automatically** message as shown in the following image.&#x20;

<figure><img src="../.gitbook/assets/image (829).png" alt="" width="375"><figcaption></figcaption></figure>

## Nightfall Events

To view the on the Nightfall Console:

1. Navigate to the **Detection and Response** from the left menu.
2. (Optional) Modify the days filter to view Events prior to last 7 days. By default the Events recorded in the **Last 7 Days** are displayed.

<figure><img src="../.gitbook/assets/image (56).png" alt="" width="563"><figcaption></figcaption></figure>

3. Apply filters to view only the GitHub Events.&#x20;

<figure><img src="../.gitbook/assets/image (1276).png" alt="" width="563"><figcaption></figcaption></figure>

Once you filter the Events to view only the GitHub Events, you can refer to the [#event-list-view](../dashboard/sdp_events/#event-list-view "mention") section to learn more about the available options.&#x20;

4. Click on any of the Events to view details of an Event. You may click anywhere in the row of an Event that you wish to inspect. Details will be present via a side panel.

<figure><img src="../.gitbook/assets/image (1258).png" alt=""><figcaption></figcaption></figure>

The side panel (or the Event detail view) is divided into three separate sections. The first section has information about the occurrence of individual findings with a preview. The third section is an activity log for the Event. Both these sections reveal information that is common across all sources/integrations. You can refer to these common sections in the [#event-detail-view](../dashboard/sdp_events/#event-detail-view "mention") section.

The second section displays details that are source / integration specific and so the details vary from one integration to the other.&#x20;

## Event Actions

Nightfall allows you to take various action on Events. When you take an action on an Event, the status of the Event changes accordingly. To learn more about Event status, refer to the [status.md](../dashboard/sdp_events/status.md "mention") document.

In GitHub, you can take actions either from the Event list view page or the Event detail view page. On the Event list view page, you can click the ellipsis menu to view the available list of actions.&#x20;

<figure><img src="../.gitbook/assets/image (1259).png" alt=""><figcaption></figcaption></figure>

On the Event detail view, you can view the applicable actions from the actions section at the bottom.

<figure><img src="../.gitbook/assets/image (1260).png" alt="" width="375"><figcaption></figcaption></figure>

To view the complete list of actions, applicable to all the integrations, you can refer to the [event\_actions.md](../dashboard/sdp_events/event_actions.md "mention") document.&#x20;

The list of actions supported for GitHub are as follows. Some of these actions are common to other integrations as well.&#x20;

* **Copy Event Link**: The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.
* **View in GitHub**: This action redirects to the relevant repository that contains the sensitive data in the source GitHub. While this action is available only on the Event detail view, please note that relevant access to the document in source GitHub repository should be present.
* **Download Original Content**: This action downloads the original content that contains sensitive data. If the content is deleted or moved to a different location within GitHub, this action fails. This action is available only on the Event detail view.
* **Send to JIRA**: This action creates a JIRA ticket for the Event. You can pick a project and Issue type while creating the JIRA ticket and can assign the JIRA ticket to the end-user
* **Acknowledge**:  You can take this action to notify other users that you have looked into this Event and will take suitable action in future.&#x20;
* **Ignore**: The ignore action flags Nightfall to ignore all the findings in the Event and may be taken if you find the findings false positive. This action marks the Event as resolved and moves it to the Resolved section. You can undo this action.&#x20;
* **Notify Email**: This action notifies the end user who added the sensitive data in GitHub about the event, through email.
* **Notify GitHub**: This action notifies the end user who added the sensitive data in GitHub about the event,  through GitHub. To learn more about how to check notifications in GitHub, see [#viewing-notifications-in-github](events.md#viewing-notifications-in-github "mention").
* **Resolve**: This action must be taken when the sensitive data is removed completely from the source file. This action resolves the Event.&#x20;

## Email Notifications

* When a data leak occurs, GitHub sends an Email notification to end users, if end users have configured Email as a Notification method in their GitHub account.
* Additionally, if Nightfall admins have configured Email Notification in [Admin Alerting](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#admin-alerting), Nightfall admins receive the Email notification.&#x20;
* If Nightfall admins have configured Email Notification in the Automation section of [End user notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification)[ ](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification)settings, end users receive an email from Nightfall. This Email allows end users to take actions from within the Email.

The Email received from by Nightfall Admins and end-users (if configured), looks as follows.&#x20;

<figure><img src="../.gitbook/assets/GIF Recording 2023-10-31 at 12.18.58 PM.gif" alt="" width="563"><figcaption></figcaption></figure>

## Viewing Notifications in GitHub

If you have configured GitHub as a Notification in the Automation section of [End User Notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification), end users can view the violation notification from within GitHub.&#x20;

Open the file that triggered the violation. A comment is generated by Nightfall which also has the remediation options. The available options are based on the settings you configured in the Automation section of [End User Notification](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-notification).&#x20;

{% hint style="info" %}
If an end-user adds sensitive information in a feature branch and merges it with the main branch, Nightfall comments on this pull request.&#x20;

If an end-user adds sensitive information in the main branch and commits it, Nightfall comments on this GitHub commit.&#x20;

The Nightfall comment is created by **nightfall-for-github** bot.&#x20;
{% endhint %}

In the following image, the Nightfall comment has two options; **Report as False Positive** and **Report as False Positive with Business Justification**. These options are displayed because they were enabled in the [End-User Remediation](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/configuring-policies/advanced-settings#end-user-remediation) section of the policy.

<figure><img src="../.gitbook/assets/GIF Recording 2023-10-31 at 12.26.25 PM.gif" alt=""><figcaption></figcaption></figure>

Additionally, if end-users have configured GitHub to receive Notifications, they can also view the violation under the Notifications page. This Notification also tags the end-user.&#x20;

To view the Violation message under GitHub notifications, end-users must execute the following steps.&#x20;

1. Click the GitHub Notifications icon.
2. Select the Notification which has a tag (mention).
3. Scroll down to view the Notification.

<figure><img src="../.gitbook/assets/GIF Recording 2023-11-16 at 8.46.25 PM.gif" alt=""><figcaption></figcaption></figure>

### Enabling Notifications in GitHub

To view Notifications from within GitHub end-users must enable the GitHub notifications. The steps to enable GitHub notifications are as follows.&#x20;

1. Click on your GitHub account icon and select **Settings**.
2. Click **Notifications** from the left pane.
3. Under **Subscriptions**, enable GitHub notifications for the **Participating, @mentions and custom** section.
4. Click **Save**.&#x20;

<figure><img src="../.gitbook/assets/GIF Recording 2023-11-16 at 9.07.55 PM.gif" alt=""><figcaption></figcaption></figure>
