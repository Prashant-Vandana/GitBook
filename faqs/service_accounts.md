---
description: >-
  Learn if you can use service accounts for authentication in the Nightfall
  integrations.
---

# Using Service Accounts with Nightfall

As a best practice, service accounts are recommended for authentication because they will not be tied to any specific user, and will persist regardless of which users may leave/join your organization. \


Also, as a security measure, it may be beneficial to provide the access privileges required to a service account, rather than having to manage permissions given to specific users. That being said, the requirements for service accounts differ by integration, as outlined below.\
\


| **Integrations**                | **Service Account Required?**     | **What will happen if the installing user leaves the company?**                                                                                                    |
| ------------------------------- | --------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **Slack**                       | **Recommended, but not required** | **If the person who authenticates leaves the company, you will be prompted to re-authenticate the next time you log in to the dashboard.**                         |
| **Google Drive**                | **Recommended, but not required** | <p><strong>If the person who authenticates leaves the company, you will be prompted to re-authenticate the next time you log in to the dashboard.</strong><br></p> |
| **Github**                      | **No need for a service account** | **If the person who installed the app on a given organization leaves, the app will continue to work without interruption.**                                        |
| **Atlassian (Jira/Confluence)** | **Recommended, but not required** | **If the person who authenticates leaves the company, you will be prompted to re-authenticate the next time you log in to the dashboard.**                         |

For any other questions/comments regarding service accounts, please contact us at [support@nightfall.ai](mailto:support@nightfall.ai). \
