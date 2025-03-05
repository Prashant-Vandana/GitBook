---
description: Learn how to get started with Confluence.
---

# Getting Started

Nightfall DLP for Confluence offers a cloud-native data leak protection solution that monitors and protects any sensitive data from leaking.

Nightfall can scan all Confluence assets (attachments, comments, spaces, blogs, and pages). Scans will include archived items, but not deleted items. Only fields of type free-text fields are scanned.

Go through the following steps before you can configure policies on your implementation of Nightfall DLP for Confluence.

* [Installing](installation/)
* [Configuring Policies](https://help.nightfall.ai/nightfall-ai/nightfall-for-confluence/configuring-policies)

## Confluence Page Restrictions

Nightfall throws an error while scanning certain pages/spaces in your Confluence instance. This issue is related to certain custom page permission restrictions for those specific Confluence pages. With base page restrictions set, the Nightfall app is unable to view edits on these page.

When **Page restrictions** are set on a page/space, our app is no longer able to see it, so when scanning is attempted on items from that page, our API requests fail. For a short term solution, you can add our app 'Nightfall DLP for Confluence' to have 'View' access on the page.\
\
**Note**: We are currently working on a longer term solution for this issue, and are in discussion with Atlassian directly

If you are not seeing these pages being scanned and want to check if this restriction is in place, this can be checked as seen below:

**Checking Workspace Permissions:**

Checking and Updating Workspace Permissions

**Checking Page Restrictions:**

Checking and Updating Confluence Page Restrictions

If you have any questions about these restrictions, or are unsure how to workaround, please file a support ticket with us, or you can reach out to support@nightfall.ai.

