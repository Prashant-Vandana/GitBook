# Scope of the Policy

In many cases, you may not need all of your data, residing in the integration, to be scanned. You might only require a specific section of your data to be scanned which is highly prone to data leakage.

The Scope stage allows you to set boundaries for monitoring. You can pick only a required section of the integration to be scanned thus reducing the noise from trusted sources. All the integrations in Nightfall (except Notion and ChatGPT) provide you the flexibility to pick and choose specific sections to include or exclude for monitoring. Nightfall scans only the data that matches the scope settings configured by you.

The configurations of the Scope stage varies for each integration. The following sections briefly describe the Scope stages for all the integrations.&#x20;

## GitHub

The GitHub integration's Scope stage allows you to select a specific GitHub org initially. Once you select the org, you can choose to scan either all of the repositories, only the public repositories, or only the private repositories from within the selected GitHub org. Once you select the required repository type (all, public, or private) to be scanned, Nightfall allows you to set conditions to exclude a specific repository (or repositories) which you do not wish to scan.&#x20;

## Microsoft Teams

The Scope stage in the Microsoft Teams integration allows you to set the scope on two entities.

a. **Chats**: The Chats section allows you to scan individual chat messages sent in MS teams. You can choose to scan either messages from all the users or specific users and groups. Furthermore, if you choose to scan messages from all the users, Nightfall optionally allows you to exclude scanning of specific users and user groups.&#x20;

b. **Teams:** The teams section allows you to scan messages shared in Teams. You can choose to scan either specific Teams or specific Teams. Within the selected team, you can choose to scan the required channels. You can also use exclusion rules to exclude specific channels or Teams.&#x20;

## Slack

The Scope stage in the Slack integration is different for Slack Pro and Business+ editions, and Slack enterprise edition.&#x20;

a. **Slack Pro and Business+**: In Slack pro and business+ editions, you can choose to monitor all the public channel, private channels, public connect channels, or private connect channels. You can choose to scan the required channel type(s). Within the selected channel type(s), Nightfall allows you to scan or exclude scanning of individual users, groups, or apps.&#x20;

b. **Slack Enterprise:** In Slack Enterprise edition, you can choose to scan either specific workspaces or specific channels. If you choose to monitor Workspaces, you can further choose to monitor all the types of channels and connect channels. Furthermore, you can choose to scan or exclude scanning of specific Users, groups, channels, or apps. &#x20;

## JIRA

The Scope stage in JIRA integration allows you to select a specific JIRA instance initially. Once you select a JIRA instance, you can choose to scan either all the projects or specific projects from the selected JIRA instance. If you choose to scan all the JIRA projects, Nightfall allows you to exclude trusted JIRA projects from being scanned.&#x20;

## Confluence

The Scope stage in Confluence integration allows you to select a specific Confluence site initially. Once you select a Confluence site, you can choose to scan either all the Spaces or specific Spaces from the selected Confluence site. If you choose to scan all the Confluence Spaces, Nightfall allows you to exclude trusted Confluence Spaces from being scanned.&#x20;

## Google Drive

The Google Drive Scope stage allows you to select all User Drives or shared drives. Within shared drives you can choose to scan either specific shared drives, exclude scanning of specific shared drives, or scan all the shared drives. Furthermore, you can also choose to scan files based on their sharing permissions. Lastly, Nightfall provides a host of filters to for granular controls. You can use the filters, to include or exclude specific users, groups, files, or labels.

## Gmail

The Gmail Scope stage allows you to scan or exclude the scanning of emails sent by specific users or user groups. Apart from senders you can also choose to scan or exclude scanning of emails sent to specific recipients and domains. &#x20;

## OneDrive

The Scope stage in OneDrive allows you to select files either based on permissions or special folders. Once you select the files based on permissions and special folders, you can choose to exclude certain files by creating specific exclusion rules.&#x20;

## Zendesk

The Zendesk Scope stage allows you to select a Zendesk instance. Once you select a Zendesk instance, you can choose to scan messages based on status of the tickets. Once you choose tickets with the required status, you can choose to exclude tickets from specific groups or agents.&#x20;

## Salesforce

The Salesforce Scope stage allows you to select a Salesforce org initially. Once you select a Salesforce org, you can choose to scan the required objects within the org, and the fields within the selected objects.&#x20;

## Best Practises to Create Policy Scope

Policy scopes allow you to configure which data to scan in your connected SaaS, GenAI applications. By carefully defining your policy scopes, you can reduce alert volume and focus on the most critical data. Here are some key considerations and best practices for creating effective policy scopes:

### **General Considerations**

* Start broad, then narrow: Begin with a wide scope and gradually refine it based on your findings and needs. You can execute a historical scan on supported SaaS apps to assess where and what types of sensitive data reside in these apps and use this information to create policies.
* Prioritize sensitive data: Focus on areas where sensitive or regulated data is most likely to be stored or shared.
* Consider your organizational structure: Align scopes with your company's departments, teams, or projects.
* Review and update regularly: As your organization changes and as you start reviewing policy violations from Nightfall, revisit and adjust your policy scopes accordingly.

### App-Specific Considerations

#### Slack, Microsoft 365 Teams

* Create scopes based on channel types such as public, private or connect channels or DMs.
* Utilize users, user groups to limit scanning of messages sent by specific users or users within specific groups.

#### Google Drive

* Use file permissions to limit the scanning of files that are externally shared or shared with external users, groups
* Leverage users, user groups synced via Okta/Google Directory/Entra ID for team or department-wise scoping. Implement label-based filtering for sensitive document categories.

#### Gmail

* Focus on external communications by filtering specific recipient domains or emails sent by specific senders, and recipients.
* Create separate policies for different departments or teams based on email patterns. For example, you may only want to monitor email communications of the support team to specific recipient domains.

#### Salesforce

* Focus on specific objects and fields containing sensitive customer data.

#### OneDrive

* Utilize file permissions to focus on shared or externally accessible content.
* Consider scoping by specific user drives for high-priority individuals.
* Use file type exclusions to ignore non-sensitive formats.
* Leverage label-based exclusions for efficient filtering.

#### Jira, Confluence

* Scope by including or excluding specific projects in Jira.
* Use space inclusions/exclusions to focus on specific areas of your knowledge base.
* Consider separate policies for public and restricted spaces.

#### GitHub

* Scope by each organization within GitHub
* Use repository pattern exclusions to ignore non-sensitive code bases.
* Implement file extension filtering to focus on specific file types.
* Utilize path exclusion to ignore non-critical areas of repositories.

#### Zendesk

* Create scopes based on ticket status to prioritize discovery and remediation of sensitive data within closed issues.

### Best Practices for Implementation

* Test policies with limited scopes before expanding.
* Monitor alert volumes and adjust scopes as needed.
* Collaborate with stakeholders from different departments to ensure comprehensive coverage.
* Regularly review and update scopes as your SaaS usage evolves.

By following these best practices and considering the unique filtering capabilities of each supported app, you can create effective policy scopes that balance comprehensive data loss prevention with manageable alert volumes.

