---
description: This document lists all the features released by Nightfall in 2025.
---

# Release Notes 2025

## June 2025

This section enlists the feature enhancements released by Nightfall in June 2025.

* **Support for macOS File Upload Blocking:** Nightfall now allows you to automatically block files with sensitive data from being uploaded to untrusted sites. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/advanced_settings/automated_action#block-transfer) to learn more about this feature.&#x20;
* **Automatic Retraining of Image ID Detectors**: The image ID detectors are now equipped with the Automated Supervised learning (ASL) system. This enhances the capabilities of the image IDE detectors. Click [here](../detection_platform/detection_glossary/) to learn more about Nightfall detectors.
* **New Driver's License Detectors**: Nightfall has now introduced new driving license detectors for the four southeast asian countries Vietnam, Thailand, Myanmar, and Cambodia. Click [here](../detection_platform/detection_glossary/) to learn more about Nightfall detectors.
* **New Search Operators for Exfiltration Events**: Nightfall has introduced new search operators in Exfiltration. You can use these operators to search specific Exfiltration events.&#x20;
* **New Upgraded Dashboard**: Nightfall has upgraded the Dashboard window completely to provide more insights and data on various aspects. Click [here](https://help.nightfall.ai/dashboard/overview) to learn more about this feature.
* **Clipboard Screen Capture Detection**: In Exfiltration, Nightfall now allows you to block users from pasting visual data (images/screenshots) to unsanctioned destinations. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste)to learn more about this feature.&#x20;
* **Clipboard Paste blocking in Windows**: In Exfiltration, Nightfall has now extended the Clipboard paste feature to Windows OS devices (previously this feature was available only in macOS based devices). Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste)to learn more about this feature.
* **User and User Group Policies in Windows**: Nightfall has extended the user and user group inclusion and exclusion feature to Windows based devices. You can now include or exclude users and user groups while creating an Exfiltration policy for Windows OS devices. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/scope#internal-users) to learn more about this feature.&#x20;
* **End user Remediation for Windows Devices**: In Exfiltration policies, Nightfall now allows you to configure end user remediation and notification. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/advanced_settings/enduser_notification) to learn more about this feature.&#x20;

## May 2025

This section enlists the feature enhancements released by Nightfall in May 2025.

* **Cloud Sync Monitoring in Windows OS**: In Exfiltration, Nightfall has now extended the cloud sync monitoring feature to devices running on the Windows OS. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#cloud-sync-app-uploads)to learn more about this feature.
* **API to Query Exfiltration and Posture Events**: In Developer APIs, Nightfall has now introduced APIs to query Exfiltration and Posture Management data. You can find the Exfiltration APIs [here](https://help.nightfall.ai/developer-api/exfiltration-prevention-apis) and the Posture Management APIs [here](https://help.nightfall.ai/developer-api/posture-management-apis).   &#x20;
* **Clipboard Paste Block Action for Windows** (early access): In Exfiltration, Nightfall now allows you to block users from pasting data to unsanctioned destinations. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste)to learn more about this feature.
* **Clipboard Monitoring of Visual Data** (early access): In Exfiltration, Nightfall now allows you to block users from pasting visual data (images/screenshots) to unsanctioned destinations. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste)to learn more about this feature.
* **Lineage Source Tracking in Windows**: In Exfiltration, Nightfall has now extended the lineage source tracking feature to devices running on the Windows OS. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#browser-uploads)to learn more about this feature.

## April 2025

This section enlists the feature enhancements released by Nightfall in April 2025.

* **Detector Enhancements**: Nightfall has now enhanced the Person Name, Street Address, and Date of Birth detectors with Automated supervised learning capabilities. Click [here](https://help.nightfall.ai/sensitive-data-protection/detection_platform/detection_glossary#standard-pii-apac) to learn more about the detectors.
* **Clipboard Paste Block Action for Windows** (early access): In Exfiltration, Nightfall now allows you to block users from pasting data to unsanctioned destinations in Windows devices (This feature is already available for macOS devices). Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste)to learn more about this feature.
* **Ability to Download Endpoint Agent Package**: In Exfiltration, Nightfall now allows you to download the agent packages for Windows and macOS devices directly from within the Nightfall console. You can find the **Download Package** button on the **Integrations** > **Endpoint** page.&#x20;
* **Ability to Exclude File & Path in Endpoints**: If a non-sensitive file is reported as an Endpoint Exfiltration event, you can now navigate to the respective event and exclude the file, file directory, or files with a same extension from being monitored in future. You can also use wildcards to define a directory pattern for exclusion. You can find these options on the [asset section](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/remediation#assets-tab) of the respective event.
* **Apply Date Range Filters on Filtered events**: Nightfall now allows you to apply date range filters on filtered event data. This allows you to view filtered events that occured during a specific date range.&#x20;

## March 2025

This section enlists the feature enhancements released by Nightfall in March 2025.&#x20;

* **Ability to Remove Disconnected Devices**: Nightfall now allows you to manually remove macOS devices from the monitored list, that are not being monitored for exfiltration. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies#removing-disconnected-devices) to learn more about this feature.
* **Stealth Deployment for macOS devices**: Nightfall now allows you to deploy the Nightfall agent in stealth mode on macOS devices so that you can now secretly install the agent without employee's knowledge. Click [here ](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/installation_mac#stealth-mode-installation)to learn more about this feature.
* **In-app Messenger**: Nightfall has now introduced an in-app chat messenger.  You can use this messenger to communicate with Nightfall support team. Just click the question mark icon on the bottom right of the screen and click **Chat**.&#x20;
* **Clipboard Paste Block Action (early preview)**: In Exfiltration, Nightfall now allows you to block users from pasting data to unsanctioned destinations. This feature is currently available for macOS devices. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/trigger#clipboard-paste) to learn more about this feature.
* **Automatic Event Resolution in Google Drive**: If you permanently delete a Google Drive file, any event generated by this file is automatically resolved. Click [here](https://help.nightfall.ai/dashboard/sdp_events/deduplication#auto-resolve) to learn more about this feature.&#x20;

## February 2025

This section enlists the feature enhancements released by Nightfall in February 2025.&#x20;

* **Support for macOS User and Group-Based Policies**: Nightfall now allows you to include or exclude specific users and user groups from being monitored by the mac policy. You can configure these settings in the filter section on the scope page of mac OS policies. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/scope#internal-users) to learn more about this feature.&#x20;
* **Support for macOS File Upload Blocking (early preview):** Nightfall now allows you to automatically block files with sensitive data from being uploaded to untrusted sites. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/advanced_settings/automated_action#block-transfer) to learn more about this feature.&#x20;
* **Support for Human Firewall (end-user remediation) in macOS Policies**: You can now configure macOS policies to notify end users about their actions that triggered violations, thus empowering them to take suitable actions. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/advanced_settings/enduser_notification) to learn more about this feature.&#x20;
* **Support to inspect content in Endpoint policies**: You can now leverage Nightfall [detection rules](https://help.nightfall.ai/detection_platform/create_detection_rules) to scan endpoint policies for sensitive data like PCI, PII, passwords, and so on. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/policies/scope#content-scanning) to learn more about this feature.&#x20;
* **Ability to Create Endpoint policies for MS Windows (early preview)**: Nightfall now allows you to create exfiltration policies for Microsoft Windows OS. Click [here](https://help.nightfall.ai/data-exfiltration-prevention/exfiltration_endpoint/install-nightfall-ai-agent-for-windows-os) to learn more about this feature.&#x20;
* **Search Filter Operators for Exfiltration Events**: Nightfall now provides you with numerous search operators to filter the Exfiltration events and view only the desired events.&#x20;
* **Introduction of Customer Referral Program**: Nightfall now allows you to refer Nightfall to your colleagues, friends and other acquintices. You can win awesome rewards with this program. Click [here](https://help.nightfall.ai/nightfall_settings/customer-referral-program) to learn more.&#x20;
* **Enhancements to the Person Name and PHI Detectors**: Nightfall has enhanced the capabilities of the Person name and PHI detectors. these detectors are now capable of generating very less false positive alerts.&#x20;
* **Introduction to Automated Supervised Learning** : With the Automated supervised learning feature, Nightfall detectors can now automate model retraining based on real-time customer feedback, thus enhancing detection accuracy. Currently, API Key and Password detectors are using this feature.  &#x20;

## January 2025

This section enlists the feature enhancements released by Nightfall in January 2025.&#x20;

* **Enhanced Detector Accuracy**: Nightfall has enhanced the detection capabilities for keys from specific vendors. These enhancements greatly reduce the rate of false positive detections. The vendors are as follows.&#x20;
  * Ping Identity
  * Auth0
  * Box
  * Plaid
  * Cohere
  * Elastic Search
  * Datadog
* **Horizontal Scaling**: Nightfall has now enhanced the machine learning infrastructure. With this improvement, the Nightfall platform is now robust enough to automatically scale to meet fluctuating demands.&#x20;
* **Introduction of Custom Branding**: You can use the custom branding feature to replace the default Nightfall logo with your organization's logo on all the alert emails generated by Nightfall. Click here to learn more about [this](https://help.nightfall.ai/nightfall_settings/custom-branding) feature.&#x20;
