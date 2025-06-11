---
description: Learn how to use the Nightfall Dashboard.
---

# Nightfall Dashboard

The Nightfall Dashboard delivers a single‑pane view of your security posture, consolidating data from every native integration in your Nightfall console. At a glance, you’ll see:

* **Active Threats**: Instantly surface and prioritize your highest‑risk alerts—click any item to jump straight to the violation details and start remediation.
* **Insights**: Analyze trends in event volume, detection accuracy, and resolution ROI to optimize your security operations continuously.
* **Environment**: Track scan volume, endpoint coverage, and capacity usage across all integrations in real-time.

Every visualization—widget, chart, or table—is interactive. Use filters for date range, integration, detector, status, and more to drill down into the exact data you need.

## Active Threats&#x20;

This section surfaces your most urgent threats in real-time so that you can address them quickly. Click any chart segment to jump straight to the corresponding violations screen—no manual searches or sorting required.

**Detection and Response Events**: This is a semi-circle visual display sall unresolved sensitive‑data events, broken out by risk level (Critical, High, Medium, Low). Click on a risk segment to navigate directly to those violations.

**Exfiltration Events**: Total exfiltration incidents logged over the last 30 days. Click to drill into the Events list and resolve threats.

**Posture Events**: This widget displays the number of posture‑related issues (e.g., misconfigurations or compliance gaps) recorded in the past 30 days. You can click the widget to drill down to the Events list and resolve them.&#x20;

**D\&C Events**: This widget displays the number of data classification events recorded in the past 30 days. You can click the widget to drill down to the Events list and resolve them.

**Encryption Events**: This widget displays the number of encryption events recorded in the past 30 days. You can click the widget to drill down to the Events list and resolve them.

<figure><img src="broken-reference" alt=""><figcaption></figcaption></figure>

## Insights&#x20;

This section enables you to monitor and optimize your security operations over time with metrics on detection accuracy, resolution efficiency, and ROI—across SecOps teams, end users, and automation.

This section displays the following widgets and charts.&#x20;

* **Events Over Time**: This bar graph displays the number of Events recorded across the selected time period. The x-axis represents time, and the y-axis represents the number of events. Data is segmented by integration, risk, policy, or resolution as applicable for the integration. You can click a bar to drill down to the list of respective events. You can also use the filter to view Event data specific to Data detection and Response, Posture, Exfiltration and data classification. Furthermore, you can also filter data based on specific time period.
* **Remediation Rate**: This widget displays the percentage of events resolved. Data is segmented as follows:
* **Remediated**: Events actively resolved to mitigate potential threats either by an Admin, End-User, or Automation.
* **Ignored**: Events that require no further action.
* **False Positives (FP)**: Events annotated as false alerts either by an Admin or End-User.
* **Business Justification**: Events dismissed with a provided business justification either by an Admin or End-User.
* **FP/Ignore Rate**: This widget displays the percentage of events that are either ignored or classified as business justified or false positives. This metric reveals the noise level in your alerting system, showing how effectively your policy triggers and detection models minimize unnecessary alerts.&#x20;
* **EU/Automation Rate**: This widget measures the proportion of event management tasks handled by end-users and automated systems as opposed to those managed manually by the security operations team.&#x20;
* **Mean Time to Resolution**: This chart displays the average time taken to resolve an event from creation to closure. It provides valuable insights into the efficiency and responsiveness of your incident management process, helping reduce resolution times and minimize the risk of exposure.

<figure><img src="../.gitbook/assets/image (1300).png" alt="" width="563"><figcaption></figcaption></figure>

*   **Most Active Policies**

    The Most Active Policies widget tracks security security events—one policy trigger each time a scanned resource contains ≥1 finding.

    * **Findings vs. Events**: Findings count individual detections (documents can have thousands); events count one trigger per resource.
    * **True Positive Events**: Policy triggers that correctly identify real security risks.
    * **Ignored Events**: Triggers you’ve chosen to dismiss.
      * **Business Justification Findings**: Annotated by admins or end-users to explain why a finding is acceptable (e.g., “Test data” or “Allowed by process”).
    * **False Positive Events**: Triggers later overturned as false alarms.
    * **Expired Events**: Triggers over 30 days old with no follow-up.

    These metrics are essential for refining your policy thresholds and cutting alert fatigue. Drill into any ignored or false-positive segment to inspect the underlying events, tweak rules or scopes, and confidently turn on automation.
*   **Most Active Detectors**

    The Most Active Detector widget tracks findings—each time our models flag sensitive data in a scanned document.

    * **Findings vs. Events**: Findings count individual detections (documents can have thousands); events count one trigger per resource.
    * **True Positive Findings**: Genuine security issues that have been resolved or confirmed.
    * **Ignored Findings**: Linked to violations you’ve dismissed.
    * **Business Justification Findings**: Annotated by admins or end-users to explain why a finding is acceptable (e.g., “Test data” or “Allowed by process”).
    * **False Positive Findings**: Marked as false alarms.
    * **Expired Findings**: Older than 30 days with no action.

    These metrics are vital for eliminating detection noise on your dataset. Your annotations feed into model retraining, boosting precision so you can safely expand automated actions. This widget is not currently clickable.
* **Highest Risk Users**: This chart provides an overview of the users generating the highest number of detection events, segmented by risk score. It helps you identify outliers and pinpoint areas where specific user behaviours or data hygiene practices may need improvement.&#x20;
* **End-User Remediation Events**: This chart provides administrators with insights into end-user resolution actions by categorising requests into:
  * **Pending**: Requests awaiting a response.
  * **Remediated**: Cases where users have taken corrective action.
  * **Justification**: Instances where a business justification led to the event being ignored.
  * **False Positive**: Cases where users have annotated the event as a false positive.

When you click a segment it opens the detailed event information in the corresponding list view for rapid review and analysis.

<figure><img src="../.gitbook/assets/image (1301).png" alt="" width="563"><figcaption></figcaption></figure>

## Environment&#x20;

Get a high‑level snapshot of your Nightfall deployment—scan volume, endpoint coverage, and capacity health—all in one place.

**Data Pack Usage**: This Data Usage widget provides an overview of your data scanning consumption versus your data purchased. Monitor usage trends and be alerted when additional capacity may be needed.

**MacOS Endpoints**: The Mac Endpoint widget shows the number of deployed endpoints for Mac devices. Quickly assess your endpoint coverage and ensure all devices are adequately protected.

**Windows Endpoints**: The Windows Endpoint widget shows the number of deployed endpoints for Windows devices. Quickly assess your endpoint coverage and ensure all devices are adequately protected.

**Data Scanned**: This widget displays the total volume of items and data scanned. Additionally, you can also view the amount of data used for scanning for each integration. Metrics for real-time scans and historical audits are provided. You can choose to view the data for the past 1 month, 3 months, 6 months, 1 year, or 2 years.

<figure><img src="../.gitbook/assets/image (1302).png" alt="" width="563"><figcaption></figcaption></figure>

## Generating Reports

Nightfall allows you download a PDF copy of the Dashboard data or email the dashboard data. If you choose to download a report, a PDF file containing the Dashboard data is downloaded.

If you choose to email the Dashboard data the following types of reports are present in the downloaded data.&#x20;

* **Sensitive Data Exposure**: This report consists of information like the location of sensitive data, the nature of sensitive data, and the overall risk associated with it.&#x20;
* **Policy Violations**: This report provides information on the policies that are generating the highest number of violations.&#x20;
* **Highest Risk Users**: This report provides information about users who are triggering the highest number of violations across all integrations.&#x20;
* **Total Data Scanned**: This report displays the total data scanned by Nightfall across all integrations.&#x20;

To email a Dashboard Report:

1. Click **Generate Reports** and select **Send to email.**
2. Select the check boxes of the reports to be included. Click **Select All** to include all the reports.&#x20;
3. (Optional) Click **Add Recipient** to add additional recipients. By default the report is mailed to the logged in user.
4. Select the time period for which you wish to download the report.
5. Click **Generate**. A pop-up window appears that confirms the Email ID to which reports will be sent.
6. Click **Done**.

<figure><img src="../.gitbook/assets/image (1303).png" alt="" width="563"><figcaption></figcaption></figure>

## Analyzing Downloaded Reports

When you generate a report, it is sent as an Email to the logged-in user. This email contains a link to download the reports. The download link expires in 7 days from the date you received the Email.&#x20;

<figure><img src="../.gitbook/assets/GIF Recording 2023-11-28 at 2.22.02 PM (1).gif" alt=""><figcaption></figcaption></figure>

A folder is downloaded to your system. The folder is named as **Nightfall\_Reports\_**_**\<date on which report was generated>\_\<historical time period>**_. This folder contains the reports that you selected for download in step 2 of the [#generating-reports](overview.md#generating-reports "mention") section. All the downloaded files are in CSV format.&#x20;

The following image shows a folder downloaded on 26-11-2023 for the last 30 days. All four reports were selected for download hence you can see four CSV files.&#x20;

<figure><img src="../.gitbook/assets/Dashboard.png" alt=""><figcaption></figcaption></figure>

### Analyzing Highest Risk Users Report

The Highest Risk Users report is named as _**\<date on which report was generated>**_**highest\_risk\_users\_**_**\<histroical time period selected>.**_ This report displays the list of users who have triggered the maximum number of violations. The users are sorted in decreasing order of violations triggered. Hence the user who caused the highest number of violations is at the top and the user who triggered the lowest number of violations is at the bottom. This report also displays the integrations, policies, and Detection rules that were violated.&#x20;

This report has the following columns.&#x20;

<table><thead><tr><th width="272">Column Name</th><th align="center">Description</th></tr></thead><tbody><tr><td>User Name</td><td align="center">The user name of the user who triggered the violation.</td></tr><tr><td>Integration</td><td align="center">The integration(s) on which the user triggered the violation.</td></tr><tr><td>Violated Policies</td><td align="center">The policy(ies) that the user violated.</td></tr><tr><td>Detection Rules</td><td align="center">The detection rule(s) that the user violated.</td></tr><tr><td>All Violations</td><td align="center">The total number of violations triggered by the user (for the time period selected in <a data-mention href="overview.md#historic-data-filter">#historic-data-filter</a>).</td></tr><tr><td>Active Violations</td><td align="center">The total number of violations that were in active status at the time the report was downloaded. </td></tr><tr><td>Actioned Violations</td><td align="center">The total number of violations that were in actioned status at the time the report was downloaded. </td></tr><tr><td>Quarantined Violations</td><td align="center">The total number of violations that were in quarantined status at the time the report was downloaded. </td></tr><tr><td>Archived Violations</td><td align="center">The total number of violations that were in archived status at the time the report was downloaded. </td></tr><tr><td>Reported Violations</td><td align="center">The total number of violations that were in reported status at the time the report was downloaded. </td></tr><tr><td>Count of Likely</td><td align="center">The total number of violations whose Likelihood was <strong>Likely</strong>, when the report was downloaded.</td></tr><tr><td>Count of Very Likely</td><td align="center">The total number of violations whose Likelihood was <strong>Very</strong> <strong>Likely</strong>, when the report was downloaded.</td></tr><tr><td>Count of Possible</td><td align="center">The total number of violations whose Likelihood was <strong>Possible</strong>, when the report was downloaded.</td></tr></tbody></table>

The following image shows a screenshot of the Highest Risk users report.&#x20;

<figure><img src="../.gitbook/assets/D2 (1).png" alt=""><figcaption></figcaption></figure>

### Analyzing Policy Violations Report

The Policy Violations report is named as _**\<date on which report was generated>\_**_**policy\_violations\_**_**\<histroical time period selected>.**_ This report displays the list of policies that triggered the violations. The policies are sorted in decreasing order of violations triggered. Hence the policy that triggered the highest number of violations is at the top and the policy that triggered the lowest number of violations is at the bottom. This report also displays the integrations, policies, detection rules, and detectors that were violated.&#x20;

This report has the following columns.&#x20;

|       Column Name       |                                                                          Description                                                                          |
| :---------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       Policy Name       |                                                  The name of the policy on which the violation was triggered.                                                 |
|       Policy UUID       |                                                  The UUID of the policy on which the violation was triggered.                                                 |
|     Policy Version      |                                             The version number of the policy on which the violation was triggered.                                            |
|       Integration       |                                                    The name of the integration to which the policy belongs.                                                   |
|     Detection Rules     |                                                     The detection rules in the policy, that were violated.                                                    |
|   Detection Rule UUIDs  |                                               The UUID of the detection rules in the policy, that were violated.                                              |
| Detection Rules Version |                                        The version number of the detection rules on which the violation was triggered.                                        |
|        Detectors        |                                                    The detectors in the detection rules that were violated.                                                   |
|      All Violations     | The total number of violations triggered by the policy (for the time period selected in [#historic-data-filter](overview.md#historic-data-filter "mention")). |
|    Active Violations    |                               The total number of violations that were in active status at the time the report was downloaded.                                |
|   Actioned Violations   |                              The total number of violations that were in Actioned status at the time the report was downloaded.                               |
|  Quarantined Violations |                             The total number of violations that were in Quarantined status at the time the report was downloaded.                             |
|   Archived Violations   |                              The total number of violations that were in Archived status at the time the report was downloaded.                               |
|     False Positives     |                                             The total number of false positive violations triggered by the policy.                                            |
|     Count of Likely     |                                The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                |
|   Count of Very Likely  |                            The total number of violations whose Likelihood was **Very** **Likely**, when the report was downloaded.                           |
|    Count of Possible    |                               The total number of violations whose Likelihood was **Possible**, when the report was downloaded.                               |

The following image shows a screenshot of the Policy Violations report.&#x20;

<figure><img src="../.gitbook/assets/D3.png" alt=""><figcaption></figcaption></figure>

### Analyzing Sensitive Data Exposure Report

The Policy Violations report is named as _**\<date on which report was generated>\_**_**sensitive\_data\_exposure\_**_**\<histroical time period selected>.**_ This report displays all the details of the sensitive data exposed. This report also displays the integrations, policies, detection rules, and detectors to which the sensitive information belongs to.&#x20;

This report has the following columns.&#x20;

|      Column Name     |                                                                                                                                                                   Description                                                                                                                                                                   |
| :------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
|       Location       | <p>The location where the leaked sensitive information resides. This can be the</p><p>project name in which sensitive data resides for the JIRA integration, the folder name for the Google Drive integration, the instance name for Zendesk, the page name for the Notion integration, and the repository name for the GitHub integration.</p> |
|     Sub-Location     |    <p>The sub-location where the leaked sensitive information resides. This can be the</p><p>URL of the ticket in which sensitive data resides for the JIRA integration, the URL for the Google Drive integration, the section name for the Notion integration, the ticket URL for Zendesk, and the file name for the GitHub integration.</p>   |
|      Integration     |                                                                                                                                      The name of the integration from where the sensitive data was leaked.                                                                                                                                      |
|   Violated Policies  |                                                                                                                              The name(s) of the policies that were violated as a result of the sensitive data leak.                                                                                                                             |
|    Detection Rules   |                                                                                                                          The name(s) of the detection rules that were violated as a result of the sensitive data leak.                                                                                                                          |
|       Detectors      |                                                                                                                             The name(s) of the detectors that were violated as a result of the sensitive data leak.                                                                                                                             |
|   Active Violations  |                                                                                                                                             The total number of active violations on sensitive data.                                                                                                                                            |
|  Actioned Violations |                                                                                                                                            The total number of actioned violations on sensitive data.                                                                                                                                           |
|  Archived Violations |                                                                                                                                            The total number of archived violations on sensitive data.                                                                                                                                           |
|   Count of Likely    |                                                                                                                         The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                                                                                                         |
| Count of Very Likely |                                                                                                                         The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                                                                                                         |
|   Count of Possible  |                                                                                                                         The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                                                                                                         |

The following image shows a screenshot of the Sensitive Data Exposure report.&#x20;

<figure><img src="../.gitbook/assets/D4.png" alt=""><figcaption></figcaption></figure>

### Analyzing Total Data Scanned Report

The Total Data Scanned report is named as _**\<date on which report was generated>\_**_**stotal\_data\_scanned\_**_**\<histroical time period selected>.**_ This report displays all the details of the data scanned.&#x20;

This report has the following columns.&#x20;

|       Column Name      |                                                                          Description                                                                          |
| :--------------------: | :-----------------------------------------------------------------------------------------------------------------------------------------------------------: |
|    Data Scanned (GB)   |                                                             The total data scanned (in Gigabytes)                                                             |
|      Items Scanned     |                                                               The total number of items scanned.                                                              |
|     All Violations     |                                                       The integrations on which the scan was performed.                                                       |
|    Active Violations   | The total number of violations triggered from the scan (for the time period selected in [#historic-data-filter](overview.md#historic-data-filter "mention")). |
|   Actioned Violations  |                                         The total number of violations that were in Actioned status (due to the scan).                                        |
| Quarantined Violations |                                                  The total number of violations that were in Actioned status.                                                 |
|   Archived Violations  |                                                  The total number of violations that were in Actioned status.                                                 |
|     False Positives    |                                                         The total number of false positive violations.                                                        |
|     Count of Likely    |                                The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                |
|   Count of Ver Likely  |                                The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                |
|    Count of Possible   |                                The total number of violations whose Likelihood was **Likely**, when the report was downloaded.                                |

The following image shows a screenshot of the Total Data Scanned report.&#x20;

<figure><img src="../.gitbook/assets/D5.png" alt=""><figcaption></figcaption></figure>
