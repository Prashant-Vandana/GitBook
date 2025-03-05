---
description: >-
  Learn what happens when both, end-user and admin apply action on sensitive
  data.
---

# I send a sensitive message, edit it, and then admin applies the Redact action. What is the outcome?

When an end-user sends a message in Slack that has sensitive data, a violation is generated on the Nightfall Violations page. If the end-user edits the message, and removes the sensitive data, and a Nightfall admin (who is unaware that the end-user has edited the message), applies either the Redact, Delete, or the Quarantine action from the [Nightfall Violations page](https://help.nightfall.ai/nightfall-ai/dashboards_violations/nightfall-violations) or from the message received in any of the[ admin notification channels](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/installation-instructions-nightfall-for-slack-1/advanced-settings#admin-alerting), the status of the Violation changes to either **Redacted**, **Deleted**, or **Quarantined** based on the action applied by the Nightfall admin. The violation log also records this action as `<<action name> by <<user name>> - time.` The edit performed by the end-user has no impact.

However, once the [deduplication feature ](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/managing-github-violations)is extended to the Slack integration, any action performed by any user, automatically changes the status of the violation accordingly.

{% hint style="info" %}
Even after applying the actions, the Slack message history displays the redacted, deleted, and quarantined messages. This is a Slack limitation.&#x20;
{% endhint %}

{% hint style="info" %}
The Redact and the Quarantine actions are available only in the Slack enterprise edition.&#x20;
{% endhint %}

