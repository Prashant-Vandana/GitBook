---
description: Learn more about the search operators provided by Nightfall, to filter Events.
---

# Event Filter Operators

This document describes all the operators provided by Nightfall to perform search operations on the Events page. You can use these operators to search for specific Events.&#x20;

Nightfall provides you with two types of operators which are described in the following sections.&#x20;

## General Operators

| Operator Name       | Description                                                                                                                                                                                                          |
| ------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| annotation\_comment | This operator allows you to filter Events using the annotation comments.                                                                                                                                             |
| annotation\_type    | This operator allows you to filter Events using the type of annotation. Nightfall provides three types of annotations. To learn more about annotations, see [#annotating-findings](./#annotating-findings "mention") |
| confidence          | This operator allows you to filter Events using the Confidence level which can either be Possible, likely, or Very Likely.                                                                                           |
| detection\_rule\_id | This operator allows you to filter Events using the unique detection rule ID.                                                                                                                                        |
| detector\_id        | This operator allows you to filter Events using the unique detector ID.                                                                                                                                              |
| file\_name          | This operator allows you to filter Events using the name of the file that triggered the violated                                                                                                                     |
| file\_type          | This operator allows you to filter Events using the type of file that triggered the violation.                                                                                                                       |
| integration\_name   | This operator allows you to filter Events using the integration name.                                                                                                                                                |
| policy\_id          | This operator allows you to filter Events using the unique ID of the policy.                                                                                                                                         |
| policy\_name        | This operator allows you to filter Events using the name of the policy.                                                                                                                                              |
| post\_context       |                                                                                                                                                                                                                      |
| pre\_context        |                                                                                                                                                                                                                      |
| quote               | This operator allows you to filter Events using the quote.                                                                                                                                                           |
| user\_email         | This operator allows you to filter Events using the email ID.                                                                                                                                                        |
| user\_name          | This operator allows you to filter Events using the name of the user who triggered the Event.                                                                                                                        |
| violation\_id       | This operator allows you to filter Events using the unique ID of the Event.                                                                                                                                          |

### Integration Operators

### Confluence Operators

#### Confluence.parent\_page\_name

This operator allows you to filter violations using the Confluence page's parent page name in which the Event was discovered.

#### Confluence.space\_name

This operator allows you to filter Events using Confluence's space name in which the Event was discovered.

### GitHub Operators

#### GitHub.author\_email

This operator allows you to filter Events using the Email ID of the GitHub user who triggered the Event.

#### GitHub.branch

This operator allows you to filter Events using the name of the GitHub branch in which the Event was triggered.

#### GitHub.commit

This operator allows you to filter Events using the GitHub commit ID in which the Event was discovered.

#### GitHub.org

This operator allows you to filter Events using the GitHub organization name in which the Event was discovered.

#### github.repository

This operator allows you to filter Events using the GitHub repository name in which the Event was discovered.

#### github.repository\_owner

This operator allows you to filter Events using the name of the GitHub repository owner in which the Event was discovered.

### JIRA Operators

#### jira.project\_name

This operator allows you to filter Events using the name of the JIRA project in which the Event was discovered.

#### jira.ticket\_number

This operator allows you to filter Events using the ticket number of the JIRA in which the Event was discovered.

### Notion Operators

#### notion.created\_by

This operator allows you to filter Events using the name of the user who created the notion page in which the Event was discovered.

#### notion.last\_edited\_by

This operator allows you to filter Events using the name of the user who last edited the notion page in which the Event was discovered.

#### Notion.page\_title

This operator allows you to filter Events using the title of the page in which the Event was discovered.

#### notion.workspace\_name

This operator allows you to filter Events using the name of the Notion workspace in which the Event was discovered.

### Slack Operators

#### Slack.channel\_id

This operator allows you to filter Events using the ID of the Slack channel in which the Event was discovered.

#### Slack.channel\_name

This operator allows you to filter vEvents using the name of the Slack channel in which the Event was discovered.

#### slack.workspace

This operator allows you to filter Event using the name of the Slack Workspace in which the Event was discovered.

### MS Teams

#### teams.channel\_name

This operator allows you to filter Events using the name of the channel in which the Event was discovered.

#### teams.channel\_type

This operator allows you to filter Events using the channel type name in which the Event was discovered.

#### teams.msg\_attachment

#### teams.msg\_importance

#### teams.sender

This operator allows you to filter Events using the name of the sender who triggered the Event.

#### teams.team\_name

This operator allows you to filter Events using the name of the team in which the Event occured.

#### teams.team\_sensitivity

### Zendesk

#### zendesk.current\_user\_role

This operator allows you to filter Events using the name of the current user who triggered the Event.

#### zendesk.ticket\_group\_assignee

This operator allows you to filter Events using the name of the group to which the Event ticket is assigned.

#### zendesk.ticket\_status

This operator allows you to filter Events using the Zendesk ticket status.

#### zendesk.ticket\_title

This operator allows you to filter Events using the name of the Ticket.
