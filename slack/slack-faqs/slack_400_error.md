---
description: >-
  Understand why Channel Management Restrictions in your Slack Workspace
  settings may be causing Slack 400 error.
---

# Upon Slack installation, why am I seeing a 400 error mentioning a "Restricted Action"?

If you see the following error on a white page, during Slack installation, this is because of a restriction in your Slack workspace of who can create private channels:\
\
`{"status":400,"detail":"failed to create notification channel: restricted_action"}`

Please follow the instructions below to remedy this issue:\
\
1\. Open your Slack Workspace settings\
\
2\. Go to the **Permissions** tab\


![](<../../.gitbook/assets/Screen Shot 2021-10-08 at 6.02.41 PM.png>)

\
3\. Expand the option for **Channel Management**\
\
4\. For the setting "**People who can create Private channels**", please set to the default option "**Everyone, plus Multi-Channel Guests (default)**"

![](<../../.gitbook/assets/Screen Shot 2021-10-08 at 6.02.54 PM.png>)

\
5\. Navigate back to the Nightfall console to complete the Slack installation. The Slack bot will now have the proper permissions required to complete the installation, as well as the private channel creation.\
\
6\. Once the installation and channel creation is complete, please feel free to revert the permissions setting back to its previous, restricted option.\
\
For reference, you can also visit [this page](https://slack.com/help/articles/115004988303-Manage-members-ability-to-create-archive-and-remove-members-from-channels) in the Slack help center, which explains how to reach this setting and the associated instructions as well.
