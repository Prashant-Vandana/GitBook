---
description: Learn how to customize the alert messages sent in Slack alerts
---

# Can we customize the alert messages sent in Slack?

You have the ability to customize notifications sent as part of Slack alerts. Previously, Slack alerts carried the same template notification, which can be seen below:

![Initial Template of Alert Notification](<../../.gitbook/assets/Screen Shot 2022-02-09 at 5.57.36 PM.png>)

You can edit the template now. This can be done as follows.

1. Navigate to the Slack integration.
2. Scroll down to the **Customize end-user notifications** sections.
3. Edit the message as required.
4. Click **Save changes**.

<figure><img src="../../.gitbook/assets/GIF Recording 2023-12-15 at 12.03.31 PM.gif" alt=""><figcaption></figcaption></figure>

## Working with Hyperlinks

To include hyperlinks in your message to end users, you must enclose the URL in <>. If you do not enclose the URL in <>, the URL is treated as plain text. So, to publish the URL www.nightfall.ai, you must draft it as follows.

`<www.nightfall.ai>`

Furthermore, to replace the URL with some other text, you must use the following syntax.

`<{link}|{hyperlinked text}>`

So, to display www.nightfall.ai as the Nightfall Home page, you must draft the message as follows.

`<www.nightfall.ai | Nightfall Home page>`

