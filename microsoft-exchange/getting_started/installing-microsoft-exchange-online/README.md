# Installing Microsoft Exchange Online

This document explains the process of installing Exchange Online. Nightfall DLP for Exchange Online allows you to scan all outgoing emails for sensitive data. Nightfall can scan both, email body and attachments.

## Overview&#x20;

When Nightfall detects emails with sensitive data, it can either Block, Quarantine, or Encrypt the email, based on the automated actions configured in the sensitive data policy for Exchange Online. You must perform the following configurations to set up monitoring of Outlook mails.

**Create Connectors**: In the Exchange Online portal, you must configure Connectors in your Exchange Online to route Emails to Nightfall to be scanned and then back to your Exchange server, once scanned.

**Create Rules**: In the Exchange Online portal, you must configure rules which enable Nightfall to route your emails.&#x20;

**Create MX Record**: You must create an MX record in the Nightfall application. This record describes your organization’s Microsoft 365 domain name and MX record.
