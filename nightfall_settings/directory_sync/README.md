---
description: Learn how you can leverage the directory sync feature in Nightfall.
---

# Directory Sync

This document explains how to integrate Nightfall with your identity providers (IdPs) like Microsoft Entra ID, Google Workspace Directory, and Okta Service. This integration simplifies policy management in Nightfall allowing you to include or exclude users and user groups, by leveraging existing user information for easier administration within Nightfall and other SaaS products.

## Advantages of Integration

* **Simplified Policy Management**: Nightfall automatically synchronises user and group information from your IDps, eliminating the need for manual user inclusions or exclusions in policies. This continuous sync ensures your policies always reflect the latest user directory information, streamlining management and reducing administrative overhead.
* **Tailored Policies with User Groups**: Leverage existing user groups defined in your IdPs to easily create granular DLP policies within Nightfall. Assign specific access and permission levels to different user groups, ensuring data security and compliance across various SaaS applications like Microsoft Teams, OneDrive, and Google Drive.
* **Dynamic User Management**: As users are added or removed from your IdP directory, Nightfall automatically reflects these changes, updating your DLP policies. This ensures your policies remain accurate and relevant, eliminating the need for manual updates.

## Configuring Directory Sync

The Directory Sync feature allows you to connect your user directories (Microsoft Entra ID and Google Workspace) with Nightfall. This sync is essential for enabling functionalities within Nightfall's SaaS apps like Microsoft 365 Teams, OneDrive for Business, Google Drive, and other apps.

* **Microsoft Teams Direct Message Monitoring (Azure Entra ID):** To monitor direct messages in Microsoft Teams for potential data leaks, Nightfall requires access to your Microsoft Entra ID account. Syncing your Entra ID account grants Nightfall a list of active users and groups, facilitating the monitoring of user communication and data flow.
* **OneDrive for Business**: To monitor user OneDrive for potentially sensitive data leaks Nightfall requires access to your Microsoft OneDrive for Business account. Syncing your Entra ID account grants Nightfall a list of active users and groups, facilitating the monitoring of user One Drives.

**Supported Identity Providers**

Nightfall currently integrates with the following IDps:

* [Microsoft Entra ID](microsoft_entra_id.md)
* [Google Workspace Directory Service](google_workspace.md)
* [Okta ](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync/adding-okta-to-nightfall)
