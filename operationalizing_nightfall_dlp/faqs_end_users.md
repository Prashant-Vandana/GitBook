---
description: Nightfall  FAQs for end-users
---

# Frequently Asked Questions (FAQs) for End-Users

## What is Nightfall?&#x20;

Nightfall is like a security guard for your organization’s digital information. It lives in the cloud and keeps an eye out for any signs of data leaks. Imagine it as a watchful friend who ensures that sensitive information doesn’t accidentally slip out. Nightfall ensures that your organization’s secrets stay safe.

You can learn more about Nightfall from [this document](https://help.nightfall.ai/nightfall-ai/introduction_to_nightfall/untitled).

## Why am I receiving Notifications from Nightfall?&#x20;

Here are some everyday situations where Nightfall steps in to protect your data:

Google Docs, Sheets, and Slides:

If you create a document, spreadsheet, or presentation with sensitive content (such as financial data or personal info), Nightfall alerts your security team which in turn may choose to alert you.

Messaging Apps (Slack, MS Teams): When you send messages containing sensitive information (maybe a credit card number or confidential project details), Nightfall gives your security team a heads-up which in turn may choose to alert you.

**Zendesk Tickets:**

Even in customer support interactions, if you accidentally add sensitive info in comments or descriptions, Nightfall intervenes.

**Code Commit on GitHub:**

When you’re working on code and accidentally include sensitive details (like passwords or private keys), Nightfall raises a flag. Your security team might choose to notify you of such an event.

These are a few examples of how Nightfall helps your organization protect sensitive data. Your security or data governance team may decide to send you additional information about best practices for your situation, invite you to take action, or for you to provide additional context to the situation.

## What's included in Nightfall notifications?&#x20;

You should expect the following information in a Nightfall notification:

Policy Information

A custom message from your organization often includes information about the data policy and best practices related to the sensitive data discovered.

Event Information

Details about the type of sensitive data including the location and time of the event

Call to action

A list of actions you can take to ensure compliance with your organization's policy or the ability to submit a business justification or report a false positive.

## What should I do now?&#x20;

Once you identify the potentially sensitive data, you can take appropriate action. The Nightfall alert displays the actions you can take. The category of actions is as follows.

* **Report as False Positive**:- If you are confident that the potentially sensitive data identified by Nightfall is not sensitive, you can choose either the Report False Positive or the Report False Positive with Business Justification actions.
* **Remove Sensitive Data or Access**:- If the Nightfall alert identified sensitive data you must take action immediately. The available actions vary for each platform. Some examples of these actions are:
  * For Slack, you can **Redact** the sensitive information or **Delete** the message.
  * For GitHub or Zendesk, you can choose to either **Redact** or **Remove** the sensitive data.&#x20;
  * For Google Drive, you can choose to **Remove access to external users**, **Restrict Link**, or **Disable Download**.&#x20;
  * For Notion, you can either **Redact**, **Remove access to external users**, or **Restrict Link**.&#x20;

**Note**: The available actions depend on the settings configured by your Nightfall administrator. If you are unable to view a specific remedial action, contact your Nightfall administrator.

## Why do I keep receiving these alerts?&#x20;

**New notifications**

Your organization may choose to notify users associated with a potential sensitive data leak or exposure risk. If you think that you have received a notification by error, make sure to report it as a false positive if this option is available to you on the notification or reach out to your data governance and security team.&#x20;

**Reminder notifications**

When the notification you receive contains a set of actions you can take, you will keep receiving reminders until you take action, submit a business justification or report as a false positive..

## What just happened? Why did my content get redacted?&#x20;

If something you sent or created was automatically removed, this means Nightfall detected what your organization considers a piece of sensitive information.  Nightfall will not remove or redact any content that your Nightfall Administrator did not explicitly instruct it to detect.

## What can I do if my content is redacted, but shouldn’t have been?&#x20;

If you are confident that any data redacted by Nightfall is not sensitive, contact your Nightfall Administrator. If the redacted data is sensitive, you need not take any further action but adhere to more safe sharing practices in the future.&#x20;

## What are the best practices I should adopt?&#x20;

Some of the best practices Nightfall recommends are:

* Be overly cautious when sharing active credentials only through approved applications or channels. If you wish to share dummy API keys or testing credentials, notify your organization's Nightfall Administrator.&#x20;
* Thoroughly check if any content that you are about to publish or share contains any sensitive data.&#x20;

## What is Sensitive Data?

Sensitive data includes information that requires special protection due to its potential impact if exposed. Examples include personally identifiable information (PII), payment card information (PCI), and protected health information (PHI). The full list varies based on the organization and the industry in which it operates.&#x20;

## Why Is Protecting Sensitive Data Crucial?

Sensitive data leaks or breaches can lead to loss of trust, financial repercussions, and legal consequences. Everyone in the organization must prioritize safeguarding this data.

\
