---
description: Learn how to apply actions on Nightfall Events.
---

# Applying Actions on Events

When an Event is registered, a Nightfall admin can take suitable action on the registered Event. The action(s) performed on an Event ensures that the prevention of sensitive data leakage. Nightfall provides a set of actions that the Nightfall admin can implement. The actions vary for each integration. You can implement an action on an Event from the Event list view or Event detail view.&#x20;

{% hint style="info" %}
While Annotations are applied to individual Findings, Actions apply to the entire Event.
{% endhint %}

When a new Event is registered, by default, the Event is assigned the **Active** status and you can find it under the **Active** tab. The **Pending** tab displays the list of violations on which you have taken some action but have not yet resolved them. The **Resolved** tab displays the list of violations that have been resolved.

{% hint style="info" %}
**IMPORTANT**

You must act on the active violations within 30 days. If you do not perform any action on an active violation within 30 days, the violation expires and moves to the **Expired** tab.
{% endhint %}



You can apply an action on a Violation either from the Violation list view page or the Violation details page, as displayed in the following image.&#x20;

<figure><img src="../../.gitbook/assets/image (1239).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
The actions menu in the detail view page displays the same list of actions as in the case of the ellipsis menu. Additionally, you can view a few more actions in the action menu which may not be present in the ellipsis menu.&#x20;
{% endhint %}

## Event Actions

The list of Actions provided by Nightfall are as follows.

### **Copy Event Link**&#x20;

The action copies the link to the Event. You can save or send this link to directly open the Event. This action is available only on the Event detail view.

### **View in \<integration name>**

This action opens the document from within the integration that contains sensitive data. This action is available only on the Event detail view.

### **Download Original Content**:&#x20;

This action downloads the file that contains sensitive data. If the file is deleted or moved to a different location within OneDrive, this action fails. This action is available only on the Event detail view.

### Ignore

This action moves the Event to the Ignored tab. For Google Drive, you can choose to Ignore multiple existing Events or future violations simultaneously. To learn more about the **Ignore all** feature in Google Drive, see [events.md](../../google-drive/policies/events.md "mention") (step 5).

### **Acknowledge**

Acknowledge action sends an email alert about the policy Event to the email account associated with your login.

### **Notify**

This action allows you to notify end users about the Event. The notification can be via Slack, Email or MS Teams (varies for each integration)

### Send to JIRA

This action allows you to select a JIRA project and create a ticket for this Event.&#x20;

### Redact

This action redacts the sensitive data found.

### Quarantine

This action temporarily moves files or sensitive data from the original place in which it was discovered to a quarantined Nightfall space for further review. You can restore the quarantined items or permanently remove them by approving or rejecting them through Nightfall alerts.

### Change Link Settings

This action modifies the link setting to anyone signed in to an account in your organization to use the link to your file.

### Disable Download

This action applies to Google Drive integration and disables download, print, and copy actions for Commenter and Viewer roles. Editor roles will retain all actions.

### Delete Attachment

This action deletes the attachment with sensitive tokens in a ticket comment (public replies and internal notes). You cannot revert this action.

### Mark as Private

This action modifies the permissions of a ticket comment from a public reply to an internal note. Converting to an internal note means the ticket comment will no longer be visible to the end user. This action is permanent.

### Remove Access

This action removes the page from the web and/or removes guest access to the page. This action is active when it applies to the page at the time of the violation

### Notify GitHub

This action is specific to the GitHub integration and sends a notification to GitHub about the violation.&#x20;

### Resolve

This action marks the violation as resolved. You can revert this action.

## Actions Supported for each Integration

The following table displays the list of all the Nightfall integrations and the Actions supported for each of these integrations.&#x20;

| Integration name |                                                                    Available Actions                                                                    |
| :--------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------: |
|    Confluence    |                    <p></p><p>Ignore<br>Acknowledge<br>Notify Slack<br>Notify Email<br>Send to JIRA<br>Redact<br>Delete<br>Resolve</p>                   |
|   Google Drive   |           <p>Ignore<br>Acknowledge<br>Notify Slack<br>Notify Email<br>Send to JIRA<br>Change Link Settings<br>Disable Download<br>Resolve</p>           |
|       JIRA       |                       <p>Ignore<br>Acknowledge<br>Notify Slack<br>Notify Email<br>Send to JIRA<br>Redact<br>Delete<br>Resolve</p>                       |
|       Slack      | <p>Ignore<br>Notify<br>Send to JIRA</p><p>Quarantine<br>Redact<br>Delete (Nightfall supports both, deletion of messages and attachments)<br>Resolve</p> |
|    Salesforce    |                                       <p>Ignore<br>Acknowledge<br>Send to JIRA<br>Redact<br>Delete<br>Resolve</p>                                       |
|      Zendesk     |  <p>Ignore<br>Acknowledge<br>Send to JIRA<br>Redact</p><p>Mark as Private</p><p>Delete Attachment</p><p>Notify Slack</p><p>Notify Email<br>Resolve</p>  |
|      ChatGPT     |                                                                 <p>Ignore<br>Resolve</p>                                                                |
|      GitHub      |                                 <p>Send to JIRA<br>Acknowledge<br>Ignore<br>Notify GitHub<br>Notify Email<br>Resolve</p>                                |
|      Notion      |      <p>Send to JIRA <br>Ignore<br>Acknowledge<br>Notify Slack<br>Notify Email</p><p>Remove Access</p><p>Delete Attachment<br>Redact<br>Resolve</p>     |
|     MS Teams     |       <p>Ignore<br>Acknowledge<br>Notify Email</p><p>Notify Slack<br>Notify Teams</p><p>Change Link Settings</p><p>Disable Download<br>Resolve</p>      |
|     OneDrive     |    <p>Ignore<br>Acknowledge<br>Notify Email<br>Notify Slack<br>Notify Teams<br>Delete File<br>Move to Recycle Bin<br>Restrict to Owner<br>Resolve</p>   |
|       Gmail      |                                         <p>Ignore<br>Acknowledge<br>Notify Email<br>Notify Slack<br>Resolve</p>                                         |

