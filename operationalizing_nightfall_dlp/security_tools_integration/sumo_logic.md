---
description: >-
  Learn how to start creating a dashboard of Nightfall alerts/actions in your
  Sumo Logic environment.
---

# Creating Dashboards for Nightfall Alerts in Sumo Logic

&#x20;If you are looking to connect Nightfall to Sumo Logic, please reference the instructions here:

{% content-ref url="siem/" %}
[siem](siem/)
{% endcontent-ref %}

Once you have gone through the Sumo Logic integration steps, we are ready to get started creating Dashboards using Sumo Logic.&#x20;

Now that the HTTP Event Collector has started receiving alerts from the webhook, you can search by a specific query or create charts to add it to a new or an existing Dashboard.

In this example, my HTTP Event Collector's name is "Minify Tax Collector". Below, you will see what a JSON payload looks like in Sumo Logic:

![This is a snippet from a Violation event in Slack](<../../.gitbook/assets/image (522).png>)

The JSON payload gives granular details like detection rules violated, policies violated, including findings and details about the sender.

![This snippet is from a Violation event in Slack](<../../.gitbook/assets/image (499).png>)

**Search:**

To search for a specific policy that was violated, click on Search and select a time frame from the dropdown menu. In this example, we will be searching for our policy titled "High Risk, Likely"

This is what our Search query would look like:

> (\_source="Minify Tax Collector") | where policiesviolated=="High Risk, Likely"

This query will list out JSON data for all instances which had "High Risk, Likely" as the policy that was violated.&#x20;

Similarly, you can search for multiple parameters too. If you want to search for a specific detection rule that was violated in the "High Risk, Likely" policy, the query would then be:

> (\_source="Minify Tax Collector") | where policiesviolated=="High Risk, Likely" && detectionrulesviolated == "Credit cards, Likely"

\
**Setting up a Dashboard for your Nightfall Alerts:**
-----------------------------------------------------

### **Step 1: Create a new Dashboard:**

From the Homepage, click on "**+New**". Click on "Dashboard". Choose a panel type, I have selected "Categorical" in this example. Enter the name of the dashboard. In this example, "Minify Tax - Nightfall" is the name of my dashboard. On the dashboard is created, the next step is to add panels/charts to the newly created dashboard.

### **Step 2: Creating a Pivot Chart**

For a basic dashboard, we will be searching for all the alerts from all services. Enter the search query:

> (\_source="Minify Tax Collector") | count by service

Select a time range. In this example, we will look at data from the past 7 days. Click on Search.\
This query will result in a pie chart which shows alerts from all the 5 services (Slack, GitHub, GDrive, Jira and Confluence).

![Panel 1: The pie chart shows Alerts from all the Services](<../../.gitbook/assets/image (516).png>)

You can customize this chart using the customization panel on the right side. Once the customization is complete, click on "Add to Dashboard" on the right. Also rename the name of the panel, in this case, the name of the pie chart/panel is "Alerts from Services". Panel name should be something that can make properties of the chart easily identifiable.

Next, we will be creating another chart to look at the different detection rules that were violated.

Select "Add Panel" to add a new panel/chart to the dashboard. Select "Categorical", enter "Last 7 days" as the date range and then enter the search query:

> (\_source="Minify Tax Collector") | where eventtype == "violation" | count by detectionrulesviolated

This query returns a list of detection rules that were violated in the last 7 days. Sumo Logic gives you the flexibility to have different time ranges in the same dashboard. You can select time period as "Last 30 days" for one panel and have a customized time period for another panel within the same dashboard. For this query, I'll be using "Bar chart" as as my chart type so it would look like:

&#x20;

![Panel 2: The bar chart shows Detection Rules Violated](<../../.gitbook/assets/image (410).png>)

### **Step 3: Adding Multiple Charts and Viewing the Dashboard:**

Step 2 can be replicated to add multiple panels to the existing dashboard.&#x20;

Here is a sample Sumo Logic - Nightfall Dashboard for your reference:

![Panel 1 shows the total violations over past 30 days;
Panel 2 shows Alerts from all Services over the past 7 days](<../../.gitbook/assets/image (653).png>)

![Panel 1 shows Detection Rules violated over the past 7 days;
Panel 2 shows Violation vs Remediation over past 30 days](<../../.gitbook/assets/image (435).png>)

![Panel 1 depicts High Risk Channels in Slack;
Panel 2 shows Highest Risk Users in Slack
](<../../.gitbook/assets/image (617).png>)

![Panel 1 shows the Policies that were violated over the past 30days;
Panel 2 shows the Remediation Action Types that were taken in the last 30 days](<../../.gitbook/assets/image (668).png>)

Please use these as a guide to get started creating your own Dashboards within Sumo Logic. If you have any questions, or would like some assistance on how to get started using Sumo Logic with your Nightfall integration, please reach out to support@nightfall.ai.
