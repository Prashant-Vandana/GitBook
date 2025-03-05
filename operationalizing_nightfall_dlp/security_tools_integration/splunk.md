---
description: >-
  Learn how to start creating a dashboard of Nightfall alerts/actions in your
  Splunk Enterprise/Splunk Cloud environment.
---

# Creating Dashboards for Nightfall Alerts in Splunk

If you are looking to connect Nightfall to Splunk, please reference the instructions here:

{% content-ref url="siem/" %}
[siem](siem/)
{% endcontent-ref %}

Once you have gone through the Splunk integration steps, we are ready to get started creating Dashboards using Splunk.&#x20;

Now that the HTTP Event Collector has started receiving alerts from the webhook, you can search by a specific query or create charts to add it to a new or an existing Dashboard.

Below, you will see what a JSON payload looks like in Splunk:

![This snippet is from a Remediation event in Slack](<../../.gitbook/assets/image (612).png>)

**Search:**

To search for a specific policy that was violated, click on Search and select a time frame from the dropdown menu. In this example, we will be searching for our policy titled "Internal Channels and Direct Messages"

This is what our Search query would look like:

> index="\*" | "policiesViolated{}"="Internal Channels and Direct Messages"

This query will list out JSON data for all instances which had "Internal Channels and Direct Messages" as the policy that was violated.&#x20;

Similarly, you can search for multiple parameters too. If you want to search for a specific detection rule that was violated in the "Internal Channels and Direct Messages" policy, the query would then be:

> index="\*" | "policiesViolated{}"="Internal Channels and Direct Messages" | "detectionRulesViolated{}"="Credentials and Secrets"

## **Setting up a Dashboard for your Nightfall Alerts:**

### **Step 1: Create a new Dashboard:**

From the Homepage, click on "Search and Reporting". Click on "Dashboards". Click on "Create New Dashboard". Enter a suitable name for your dashboard. Choose the type of dashboard you would like to create- Classic/Studio. Click "Create".

Once the dashboard is created, it is displayed in the list of dashboards.

### **Step 2: Creating a Pivot Chart:**

Navigate to the "Search & Reporting" tab. You can create a chart by either entering a search query or navigating to the "Visualization" section.

For a basic search, enter a query like:

> index="\*"&#x20;

Go to "Visualization" tab, select "Pivot".

![](<../../.gitbook/assets/image (605).png>)

Next, you can either select "All Fields" or "Selected Fields"; these are the fields you would like to use as your Data Model.&#x20;



![](<../../.gitbook/assets/image (651).png>)

Select "Pie Chart" to create a pie chart to show all the detection rules that were violated.

Next, you can click on the dropdown for "Range" to choose the timeframe/time range you want the data to be from.&#x20;

![](<../../.gitbook/assets/image (474).png>)

Next, select "detectionRulesViolated{}" from the "Field" and "Color" dropdown. You can also create a custom label and give it a name.



![This chart will show the different top Detectors that are triggered in the Violations](<../../.gitbook/assets/image (494).png>)

If you hover over any of the pieces of the pie, it displays specific details about the detection rule that was violated and also displays the number of times it was violated.

&#x20;

![This highlights our 'Credentials and Secrets' Detection Rule and gives us some key metrics, such as number of violations as well as overall percentage compared to other Rules](<../../.gitbook/assets/Screen Shot 2022-02-02 at 4.44.45 PM.png>)

Once the pie chart has been created, click on "Save As" > "Dashboard Panel". Select the "Existing Dashboard Panel" that was created in Step 1. Make sure to select the name of the dashboard from the list. Panel title would be the title of the panel. e.g. "Detection Rules Violated" and give a unique model id. e.g. detectionrules. Click on "Save"

### **Step 3: Adding Multiple Charts and Viewing the Dashboard:**

Steps 1 and 2 can be used to create multiple charts and to add them to an existing dashboard.



Finally, here are some sample Nightfall-Splunk Dashboard examples:

![This above view breaks down the violation by the following: by Policy, by Detection Rule, by Channel](<../../.gitbook/assets/image (480).png>)

![Here, we can visualize the total number of Alerts and Actions that are occurring over 3 different integrations: Slack, Google Drive, and Github](<../../.gitbook/assets/image (428).png>)

![In this view, we can break down the Remediation actions that have taken place, broken down by the specific action. Also, we can tally our most consistent Nightfall violators.](<../../.gitbook/assets/image (501).png>)

\
Please use these as a guide to get started creating your own Dashboards within Splunk. If you have any questions, or would like some assistance on how to get started using Splunk with your Nightfall integration, please reach out to support@nightfall.ai.&#x20;
