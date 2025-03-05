---
description: Understand the requirements for Nightfall DLP for Slack Enterprise.
---

# Requirements for Nightfall DLP for Slack Enterprise

Ensure the following requirements are fulfilled before you get started.

* **You must enable the Slack Discovery API before getting started with Nightfall.** You can confirm or request this by writing to Slack at [feedback@slack.com](mailto:feedback@slack.com).
* A service account with appropriate Slack permissions is required.
  * For Slack Enterprise Grid plans, an Org Owner is required and must be a member of at least one of the workspaces. Org Primary Owner is not required.
  * For Slack Enterprise Select plans, a Workspace Owner is required. Workspace Primary Owner is not required.
* The Channel Management permission for **“People who can create Private channels”** must be set to **“Everyone, plus Multi-Channel Guests (default)”**. See [this](https://slack.com/intl/en-gb/help/articles/115004988303-Adjust-channel-management-permissions#enterprise-grid-subscription-3) article for instructions on how to check and set this permission. Once you have completed the installation, you can revert the permission to its original setting.

<figure><img src="../../../.gitbook/assets/image (343).png" alt=""><figcaption></figcaption></figure>

* While not a requirement for installation, in order for Nightfall to scan edits in direct messages, Slack’s Retention Policy must be set to “Keep all messages, including revision history.” Please review [this](https://slack.com/help/articles/203457187-Customize-message-and-file-retention) article for information on configuring this policy.
