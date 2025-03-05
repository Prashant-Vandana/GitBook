---
description: Learn how to install the Nightfall DLP for Gmail.
---

# Install Nightfall DLP for Gmail

This document explains the process of installing Nightfall DLP for Gmail. Nightfall DLP for Gmail allows you to scan all outgoing emails for sensitive data. Nightfall DLP for Gmail can scan both, email body and attachments.&#x20;

## Prerequisites

* You must have a Google Workspace account.
* You must have administrator access to the above Google Workspace account.

## Overview&#x20;

When Nightfall detects emails with sensitive data, it can either Block, Quarantine, or Encrypt the email, based on the automated actions configured in the sensitive data policy for Gmail. To enable Nightfall to perform the quarantine action, you must set up compliance rules in Google Workspace.&#x20;

Once you set up the compliance rules, you must then configure routing rules to setup the SMTP relay service to receive emails from Nightfall.

