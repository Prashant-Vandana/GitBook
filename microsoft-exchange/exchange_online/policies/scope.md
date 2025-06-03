---
description: Learn how to configure the Scope section for Exchange Online.
---

# Configure Scope for Exchange Online

The Scope section allows you to select specific mailboxes to be monitored. Once you select the mailboxes, you can further add granular level filters to only monitor emails from specific senders and recipients.&#x20;

**Note**: If you have configured multiple Microsoft tenants in Nightfall, you must first select the tenant to be monitored.&#x20;

Nightfall provides the following sections on the Scope page.&#x20;

**Mailboxes**: In this section, you can choose to monitor only specific senders, recipients, or groups. Conversely, you can exclude the monitoring of specific senders, internal recipients, or domains.

**Recipients and Domains**: In this section, you can apply filters to monitor only external recipients and domains. Conversely, you can exclude the monitoring of specific external recipients, or domains.

## Mailboxes

1. Click **+ Add Tenant** and select a **Microsoft tenant**.&#x20;
2. Click **+ Add Filter** and select one or multiple described as follows.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXcVVCXuo1pD7qgVCdVNcLkUrVMaI7pC8oN4hqEDJqX3RkzxCp7Fy4JFFtesPLq2qAoP0E2fP2Jo0R_H_0L8WM1tbNhEWfG-V6fIiTfuHrkhtMhw6BnQinqRGUpCV8I_QK49ewenXw?key=gXxqXq4O-toSF3b-7YIbPg" alt="" width="563"><figcaption></figcaption></figure>

### Mailboxes - Senders

You can use this filter to only monitor or exclude the monitoring of emails sent by specific senders.&#x20;

* **Only Include**: You can use this option to only monitor mails sent by specific users. Once you select this option, you must also select the required users from the drop-down menu. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent by specific users. Once you select this option, you must also select the required users from the drop-down menu.

### Mailboxes - Sender User Groups

You can use this filter to only monitor or exclude the monitoring of emails sent by users who are part of specific sender groups.&#x20;

* **Only Include**: You can use this option to only monitor mails sent by specific sender user groups. Once you select this option, you must also select the required sender user groups from the drop-down menu. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent by specific sender user groups. Once you select this option, you must also select the required sender user groups from the drop-down menu.

### Mailboxes - Recipient User Groups

You can use this filter to only monitor or exclude the monitoring of emails sent to users who are part of specific recipient groups.

* **Only Include**: You can use this option to only monitor mails sent to specific recipient user groups. Once you select this option, you must also select the required recipient user groups from the drop-down menu. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent to specific recipient user groups. Once you select this option, you must also select the required recipient user groups from the drop-down menu.

### Mailboxes - Internal Recipients

You can use this filter to only monitor or exclude the monitoring of emails sent to internal recipients.

* **Only Include**: You can use this option to only monitor mails sent to internal recipients. Once you select this option, you must also select the required users from the drop-down menu. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent to internal recipients. Once you select this option, you must also select the required users from the drop-down menu.

<figure><img src="../../../.gitbook/assets/image (1296).png" alt=""><figcaption></figcaption></figure>

Click **Next** once you have configured all the required filters.&#x20;

## Recipients and Domains

You can use this section to apply filters on external recipients and domains. This section provides the following filters.&#x20;

### External Recipients

You can use this filter to either monitor all the mails sent to external recipients, only monitor specific external recipients or exclude the monitoring of specific external recipients.&#x20;

* **Monitor All**: This option monitors all the emails sent to external recipients.&#x20;
* **Only Include**: You can use this option to only monitor mails sent to external recipients. Once you select this option, you must also select the required users from the drop-down menu. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent to external recipients. Once you select this option, you must also select the required users from the drop-down menu.

### Recipient Domains

You can use this filter to monitor emails sent to recipient domains. You can also use wild cards to match multiple domains.&#x20;

* **Monitor All**: This option monitors all the emails sent to all the domains.&#x20;
* **Only Include:** You can use this option to only monitor mails sent to specific domains. Once you select this option, you must also enter the domain names to be included for monitoring. &#x20;
* **Exclude**: You can use this option to exclude the monitoring of mails sent to specific domains. Once you select this option, you must also enter the domain names to be excluded from being monitored.

**Note**: You can use[ this link](https://regex-generator.olafneumann.org/?sampleText=2020-03-12T13%3A34%3A56.123Z%20INFO%20%20%5Borg.example.Class%5D%3A%20This%20is%20a%20%23simple%20%23logline%20containing%20a%20%27value%27.\&flags=i) to generate a regular expression that exactly matches your domain requirements.

<figure><img src="../../../.gitbook/assets/image (1297).png" alt=""><figcaption></figcaption></figure>
