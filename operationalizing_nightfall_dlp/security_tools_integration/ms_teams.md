---
description: >-
  Learn how to configure Nightfall to send alerts to Microsoft Teams using
  email.
---

# Sending Alerts to Microsoft Teams

Integrating your Nightfall alerts to Microsoft Teams for Slack/Jira/GDrive/Confluence can be done using the following the steps:

1. Log in to your Microsoft Teams account and create a new channel called "Nightfall Alerts". You can also use your existing channel to send your alerts to it. Click on the three dots next to the channel name, "More options"

![Snippet when you hover over the three dots (More options)](<../../.gitbook/assets/Screen Shot 2022-06-27 at 2.06.44 PM.png>)

2\. Select "Get email address" in more options.

![This is a snippet when you click on the three dots next to Channel name In Teams](<../../.gitbook/assets/Screen Shot 2022-06-27 at 2.10.35 PM.png>)

3\. Copy the email address shown in the pop-up:

![Snippet which shows email address of a Teams Channel](<../../.gitbook/assets/Screen Shot 2022-06-27 at 2.14.45 PM.png>)

4\. Log in to your [Nightfall](http://app.nightfall.ai) account, click on the integration you want to integrate with. In this example, I have selected "Jira":

![Snippet of Jira integration in Nightfall's UI](<../../.gitbook/assets/Screen Shot 2022-06-27 at 2.18.24 PM.png>)

5\. Click on "Settings" and in the "Email alert" textbox, enter the Microsoft Teams email address from Step 3 and Save it.

![Snippet shows the textbox where you can send your alerts to](<../../.gitbook/assets/Screen Shot 2022-06-27 at 2.20.49 PM.png>)

Once a policy is violated, you should an receive alert in your Teams channel:

![Snippet in MS Teams of a violation (Credentials & Secrets), API key was detected by Nightfall](<../../.gitbook/assets/image (412).png>)

You can also take remediation actions like "Redact Findings" or delete (in case of attachment) through Microsoft Teams.\
\
For any issues or questions, please feel free to reach out to support@nightfall.ai.&#x20;
