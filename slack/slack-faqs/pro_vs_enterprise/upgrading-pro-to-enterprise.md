---
description: Learn how to migrate from Slack Pro to Slack Enterprise edition
---

# Upgrading from Slack Pro to Enterprise

## **Overview**

The upgrade from Nightfall Pro for Slack to Nightfall Enterprise for Slack will take approximately 30 minutes to complete. Nightfall will guide you through this process with the support of the Nightfall Customer Success, Product Management, and Engineering teams. The Slack Discovery API must be enabled on your Slack account in order to complete the upgrade.

## **Uninstalling Nightfall Slack Integration**

The process will begin by having your Slack workspace owner uninstall the Nightfall Pro for Slack application from your Slack environment. This will remove the application from the Slack environment and also remove the Nightfall bot from all Slack channels it has joined (Nightfall will discontinue use of the custom auto-join script). The bot does not post any messages or notifications to a channel when it leaves - this will occur silently and without disruption to end-users. Lastly, the current Nightfall alerting channel will need to be deleted in your Slack environment. (NOTE: Please be sure to export all required audit data from this channel prior to deletion.)

## **Installing Nightfall Slack Enterprise Integration**

Once the Nightfall Pro application has been uninstalled, the Nightfall admin console will prompt you to install the Slack Enterprise application. The two steps included are to:&#x20;

1. Authorize the Nightfall application to use the Slack Discovery API
2. Install the Nightfall application into your Slack workspace.

Once installation is complete, the Nightfall application will automatically create three new private Slack channels (#nightfall-alerts-slack, #nightfall-content-slack, and #nightfall-quarantine-slack) in the chosen Slack workspace. The user that installed the Nightfall application will be the sole member of those private channels and will need to invite any additional required administrators to those channels (the recommended method for invitation is using the following command in each of the Slack channels "/invite @\[user to invite]"). Alerts for violations in all workspaces will be generated and triaged in these Slack channels.

## **Method of Monitoring**

While the Nightfall Pro application scans files and messages at the channel level (requiring it to be invited manually or automatically into any channel that customer would like to monitor), the Nightfall Enterprise application leverages the Slack Discovery API for detection and classification. This allows the Enterprise application to operate without invitation to individual channels or exposure to end users. The Nightfall bot will not join any individual channels or post any notifications or messages to channels notifying the end-user about monitoring, unlike Nightfall Pro (this includes newly created channels as well).&#x20;

Rather than segmenting channels by choosing which channels to invite the bot to, with the Enterprise application, you’ll segment channels by selecting channel types and workspaces to monitor in the Nightfall admin console (options for individual channel whitelisting are managed here as well).

## **Additional Feature: Quarantine**

With the upgrade to Nightfall Enterprise, you’ll now have the ability to inspect findings via quarantine functionality and the #nightfall-content-slack channel. When an alert is generated in #nightfall-alerts-slack, a third option ("Quarantine") will now be available (in addition to the existing "Approve" and "Delete" options).

Quarantining a sensitive item will result in the original message/file being removed from its context and replaced with a tombstone message, visible to the sender and any other members of the channel.

For a full list of features & differences between Nightfall Pro and Enterprise, please review our comparison chart [here](https://docsend.com/documents/1860121).

## **Analytics**

One feature in the old product that is not yet supported in the new product, but is coming soon, is the Analytics Dashboard. This includes the ‘Download as CSV’ feature.&#x20;

However, Nightfall will still send you Weekly Analytics Summary emails. Additionally, any analytics data needed can be manually compiled for you as needed. For ad-hoc analytics data requests, please contact your Customer Success Manager.

## **Recommendation: Install Nightfall Slack App using a Machine User**

For the initial authentication to Slack, a machine/service account user is recommended but not required - if the person who installs the app leaves the company, you will be prompted to reinstall the next time that you log in to the dashboard.&#x20;

If you have any questions, please reach out to your Customer Success Manager or to [support@nightfall.ai](mailto:support@nightfall.ai).
