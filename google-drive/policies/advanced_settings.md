---
description: >-
  Learn how to configure the advanced settings section in a Nightfall policy for
  the Google Drive.
---

# Configure Advanced Settings for Google Drive

This stage allows you to select notification channels if a policy violation occurs. The notification alerts are sent at two levels; **admin** and **end-user.** Admin users are the Nightfall administrators who generally work on the Nightfall SaaS application and configure various settings in Nightfall. End-users are owners or editors of the file in which the violation was detected.&#x20;

## Admin Alerting

This section allows you to send notifications to Nightfall users.&#x20;

{% hint style="info" %}
The alert configurations configured in this section describe the process of creating alerts at the policy level. Policy-level alerts apply only to the policy on which they are configured. To configure an alert on all the Google Drive policies, you must configure alerts at the integration level. To learn more about how to configure integration-level policies for the Google Drive integration, read [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-google-drive/installation-instructions-nightfall-for-google-drive/copy-of-configuring-integration-alerts).
{% endhint %}

The steps to configure alert channels for policy-level integration are the same as in the case of integration-level alerts. You can refer to [this document](https://help.nightfall.ai/nightfall-ai/nightfall-for-google-drive/installation-instructions-nightfall-for-google-drive/copy-of-configuring-integration-alerts#configure-alerts-at-the-integration-level) for steps.

## Automated Actions

This section describes the various actions that Nightfall takes automatically when a violation is detected. You must turn on the toggle switch to enable an action. All the automated actions are permanent and cannot be reversed once applied. You can also use the **delayed remediation** feature to set the timeline as to when an action must be taken. You can either choose to apply the automated action immediately after detecting a violation or after some time.&#x20;

The various automated actions are described as follows.

* **Remove all external users and groups:** This action revokes the file access in which sensitive data was found. All external users and groups will no longer have access to the file. You must also configure the **delayed remediation** feature by selecting an option in the **Trigger action** field. You can either choose to apply the action You can either select the I**mmediately** option to apply the automated action immediately after detecting a violation or select the **After** option to implement the automated action after a certain time delay. If you select the **After** option, you must also set the delay time. The automated action is implemented once the delay time is elapsed.&#x20;

<figure><img src="../../.gitbook/assets/image (1230).png" alt=""><figcaption></figcaption></figure>

* **Remove all internal users and groups:** This action revokes the file access in which sensitive data was found. All internal users and groups will no longer have access to the file.&#x20;
* **Restricted**: This action restricts the file access only to those users who have the link to access it.
* **Disable Download, Print, and Copy**: This action disables downloading, printing, or copying the file in which sensitive data was found. This action is only applicable to users with the **View** and **Comment** permission. File owners can always download and copy the file.
* **Apply Labels**: This action allows you to automatically apply labels on files with sensitive data. You can choose to apply either a **badged label** or **standard labels**. All the Labels are listed under the + **Add Label** drop-down menu. You must click this drop-down menu and select the required label(s).&#x20;

<figure><img src="../../.gitbook/assets/image (1280).png" alt=""><figcaption></figcaption></figure>

### Automated Action Scenarios

#### Change Link Settings to Restricted

**Action Description**

When executed, this action removes any existing **Anyone with the link** sharing settings. Disables public access to the file and limits access to only specifically designated users and groups. The sharing settings are updated to Restricted.

**Supported Scenarios**:

* Files stored in user's personal drive
* Files located in shared drives
* Files currently configured with "Anyone with the link" access
* Files currently shared with specific target audiences

**Unsupported Scenarios**

* Files already set to "Restricted" access level

#### Remove External Users & Groups

**Action Description**: When executed, this action has a different impact on files that are part of a personal drive and files that are part of a shared drive.&#x20;

**For files in personal drives**:

* Identifies all external users and groups (outside the organization domain)
* Removes their access permissions
* Maintains internal user permissions
* Preserves owner access

**For files in Shared Drives:**

* Removes only directly assigned external users and groups.
* However, external users and groups with access to the shared drive can continue accessing the file.

**Supported Scenarios**:

**Personal Drive Files**:

* Removes all external users and groups
* File owner retains access

**Unsupported Scenarios**:

**Shared Drive Files**:

* External users with shared drive access retain their access
* Permission inheritance from the shared drive cannot be overridden

#### Remove Internal Users & Groups

**Action Description**: When executed, this action has a different impact on files that are part of a personal drive and files that are part of a shared drive.&#x20;

**For Personal Drive Files**:

* Identifies all internal users and groups (within the organization domain)
* Removes their access permissions
* Maintains owner access

**For Shared Drive Files**:

* Identifies directly assigned internal users/groups and removes only direct permissions.
* Preserves drive-level access

**Supported Scenarios:**

**Personal Drive Files:**

* Removes all internal users and groups
* File owner retains access

**Shared Drive Files:**

* Removes only directly assigned internal users and groups
* Drive collaborators retain their access

#### Disable Download, Print and Copy

**Action Description**: When executed, this action:

* Removes the ability to download the file
* Disables printing functionality
* Prevents copying of file content
* Maintains view/edit access based on existing permissions

**Supported Scenarios**:

* Files in user's personal drive
* Files in shared drives
* Files where these actions are currently enabled

**Unsupported Scenarios**:

* Files where these actions are already disabled
* File types that don't support permission restrictions

## End-User Notification

This section allows you to configure notifications to be sent to the end user whose actions triggered the violation.&#x20;

### Custom Message

Enter a custom message to be sent to the end user. This message is sent in an Email. You can modify the default message provided by Nightfall and draft your message. The total character length allowed is 1000 characters. You can also add hyperlinks in the custom message. The syntax is \<link | text >. For example, to hyperlink [https://www.nightfall.ai](https://www.nightfall.ai/) with the text **Nightfall website**, you must write  \
<[https://www.nightfall.ai](https://www.nightfall.ai/) | Nightfall website> .

<figure><img src="../../.gitbook/assets/image (773).png" alt=""><figcaption></figcaption></figure>

### Automation

You can select one of the following methods. You must turn the toggle switch to use this option.

* **Via Slack:** This option sends a Slack notification to the user whose actions triggered the violation.  &#x20;
* **Via Email:** This option sends an Email to the user whose actions triggered the violation.&#x20;

<figure><img src="../../.gitbook/assets/image (774).png" alt=""><figcaption></figcaption></figure>

### End-User Remediation

End-user remediation (also known as Human Firewall) allows you to configure remediation measures that end users can take, when a violation is detected on their Google Drive files. You must turn on the toggle switch to use this option. When an end-user action triggers a violation, they receive an email with content mentioned in the [#custom-message](advanced_settings.md#custom-message "mention") section. Apart from the Email content, end users can also view one or multiple actions described below. All the actions that a Nightfall admin enables here, are visible to end-users in the Email.&#x20;

* **Remove External User(s):** This action revokes the file access permissions. All external users lose access to the file in which sensitive data was found. If you have enabled the **Remove all external users and groups** action in the [#automated-actions](advanced_settings.md#automated-actions "mention") section, this action is disabled.
* **Restricted Link**: This action resets the file access permission to only those users who have the link to the file. If you have enabled the **Restricted** action in the [#automated-actions](advanced_settings.md#automated-actions "mention") section, this action is disabled.
* **Disable Download**: This action disables the download of the file in which sensitive data was found. If you have enabled the **Disable Download, Print, and Copy** action in the [#automated-actions](advanced_settings.md#automated-actions "mention") section, this action is disabled.
* **Apply Labels:** This action allows end-users to apply either **badged label** or **standard labels** on the files with sensitive data. End-users can apply a single badge label and up to four standard labels.  If you have enabled the **Apply Labels** action in the [#automated-actions](advanced_settings.md#automated-actions "mention") section, this action is disabled.
* **Report as False Positive with Business Justification**: This option allows end users to report false positive alerts and provide a business justification as to why the alert is considered to be false positive.&#x20;
* **Report as False Positive**: This option allows end users to report false positive alerts.

**When a Violation is Reported as False Positive**: You can use this option to set actions to be taken when a violation is reported as false positive by the end-user. You can either set the remediation to be automatic or manual.&#x20;

**Remind Every (until Violation expires)**: You can use this option to set a reminder for the end-user to take action on the violation. You can choose to remind the end user every 24, 48, or 72 hours.

<figure><img src="../../.gitbook/assets/image (1078).png" alt=""><figcaption></figcaption></figure>



