---
description: Learn the permissions required for each Nightfall integration.
---

# Which permissions are required for each integration?

Please find the permissions required for each integration, in the table below:\
\
**Native Integrations:**

<table><thead><tr><th width="150">Integrations</th><th width="399.3333333333333">Permissions Required</th><th>Roles Required for install</th></tr></thead><tbody><tr><td>Slack</td><td><p>You can create private channels in Channel Management Permissions. </p><p></p><p>To create, Select the default option - Everyone, plus multi-channel guests.</p><p></p><p>Nightfall Enterprise DLP for Slack uses three user token scopes:</p><ul><li>discovery:read </li><li>discovery:write </li><li>groups:write</li></ul><p>Nightfall Enterprise DLP for Slack has 13 Bot Token Scopes: </p><ul><li>Channels:join</li><li>Channels:read</li><li>Chat:write</li><li>Commands</li><li>Files:read</li><li>Files:write</li><li>Groups:read</li><li>Groups:write</li><li>Im:read</li><li>Im:write</li><li>Mpim:read</li><li>Users:read</li><li>Users:read.email</li></ul><p>Nightfall Pro DLP for Slack has 26 Bot Token Scopes: </p><ul><li>Channels:history</li><li>Channels:join</li><li>Channels:manage</li><li>Channels:read</li><li>Chat:write</li><li>Chat:write.public</li><li>Commands</li><li>Conversations.connect:read</li><li>Files:read</li><li>Files:write</li><li>Groups:history</li><li>Groups:read</li><li>Groups:write</li><li>Im:history</li><li>Im:read</li><li>Im:write</li><li>Mpim:history</li><li>Mpim:read</li><li>Mpim:write</li><li>Reminders:read</li><li>Reminders:write</li><li>Team:read</li><li>Usergroups:read</li><li>Usergroups:write</li><li>Users:read</li><li>Users:read.email</li></ul><p>Nightfall Pro DLP for Slack has nine User Token Scopes: </p><ul><li>Admin.conversations:read</li><li>Admin.conversations:write</li><li>Channels:read</li><li>Channels:write</li><li>Chat:write</li><li>Files:write</li><li>Groups:read</li><li>Mpim:write</li><li>Users:read</li></ul></td><td><p>Slack Workspace Owner - Pro<br></p><p>Slack Org Owner - Enterprise</p></td></tr><tr><td>Google Drive</td><td><p>The following access permissions are required:</p><p>https://www.googleapis.com/auth/admin.directory.user.readonly,</p><p>https://www.googleapis.com/auth/admin.directory.group.readonly, https://www.googleapis.com/auth/admin.directory.group.member.readonly, https://www.googleapis.com/auth/admin.directory.domain.readonly, https://www.googleapis.com/auth/drive</p></td><td>Google Super Admin</td></tr><tr><td></td><td><p>Access to the following is required:</p><ul><li>User Read</li><li>Group Read</li><li>Billing Read</li><li>Domain Management</li><li>Domain Settings</li><li>Services > Drive and Docs > Settings: List Companies Shared Drives</li></ul></td><td>Google Service Account</td></tr><tr><td>Confluence</td><td><p>Space Permissions: </p><ul><li>All - View </li><li>Pages - Add</li><li>Delete Blog - Add</li><li>Delete Comments - Add</li><li>Delete Attachments - Add</li><li>Delete Space - Admin</li></ul></td><td>Confluence Admin</td></tr><tr><td>Jira</td><td><p>Nightfall for Jira can perform the following actions on your behalf:</p><ul><li>Create and manage issues: Create and edit issues in Jira, post comments as the user, create worklogs, and delete issues.</li><li>View Jira issue data: Read Jira project and issue data, search for issues, and objects associated with issues like attachments and worklogs.</li><li>View user profiles: View user information in Jira that the user has access to, including usernames, email addresses, and avatars.</li></ul></td><td>Jira Admin</td></tr><tr><td>Github</td><td><p>To enable integration, Read access to the following is required: </p><ul><li>Code</li><li>Commit statuses</li><li>Members</li><li>Metadata</li></ul></td><td>Github Organization Owner</td></tr><tr><td>Salesforce</td><td><p>Nightfall DLP connected app package required the following permissions: </p><ul><li>Access to identity url service </li><li>Access content resources </li><li>Manage user data via APIs </li><li>Perform requests at any time</li></ul></td><td>A dedicated user with system administrator privileges in Salesforce can install the connected app package, and grant access to Nightfall via OAuth.</td></tr></tbody></table>



**Alert Platforms:**

| Alert Platform | Permissions Required for Install |
| -------------- | -------------------------------- |
| Slack          | Slack Workspace Owner            |
| Jira           | Jira Admin                       |

\
\
For more information on which integrations/platforms would require/recommend a service account, please refer the page below:

{% content-ref url="service_accounts.md" %}
[service\_accounts.md](service_accounts.md)
{% endcontent-ref %}
