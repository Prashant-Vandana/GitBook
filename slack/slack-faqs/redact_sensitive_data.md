---
description: Redacting Sensitive Messages in Slack
---

# Can I redact sensitive message content in Slack?

In the Slack integration, you are able to use redaction as a remediation action for messages. Similarly to how you can notify, quarantine, or delete messages, you can also choose to redact the sensitive info out of messages, so that only the first two characters of the sensitive token are shown, and the rest of the message is then shown as a set of \*\*\* characters. (Note: Redaction is only available for messages, and cannot be used for images/files shared in Slack)\
\
This is available in the Slack Enterprise integration. Please find some screenshots below, for what this workflow may look like.

1. A potential sensitive message is posted in a channel that is being monitored by a Nightfall Slack policy:

![](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.52.30 PM.png>)

2\. The Nightfall Alert is Generated:

![](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.51.37 PM.png>)

3\. Once the 'Redact message' option is chosen:

![](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.51.49 PM.png>)

4\. Once you confirm you would like to redact the message:

![An audit log is generated showing that a redaction action was taken on the message](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.51.59 PM.png>)

![The original message has now been redacted](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.52.12 PM.png>)

You can now see the redacted message in the original message location, as well as a small message that notifies the user their message has been redacted as it may contain sensitive information.

#### Automated Redaction

In the Slack Policy itself, it will be shown in the list of Automated actions, along with the other remediation actions as well:\


![You can use this option from the console to automatically redact sensitive messages within Slack](<../../.gitbook/assets/Screen Shot 2022-02-07 at 6.53.11 PM.png>)
