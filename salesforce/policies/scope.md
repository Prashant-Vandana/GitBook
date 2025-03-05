---
description: Learn how to configure the Scope section in the Nightfall DLP for Salesforce.
---

# Configure Scope for Salesforce

The Scope stage allows you to select the Salesforce org in which the policy can be created.&#x20;

To configure Policy Scope:

1. Click **+ Add Org** and select a Salesforce org.
2. Select the Salesforce object that must be scanned by Nightfall. Currently, Nightfall only displays the standard Salesforce objects.
3. Select the check box for the Salesforce fields that must be scanned by Nightfall. Nightfall displays a list of Salesforce fields (from the selected Salesforce Object) that are vulnerable to data leaks (including custom fields). This includes fields whose data type is Number, Name, Description, and so on.&#x20;

{% hint style="info" %}
You must select the **Select all** check box to include all the displayed fields for scanning.
{% endhint %}

4. (Optional) Click the **<-** arrow to navigate back to the Object list, select another object, and subsequently the fields of the objects to be scanned.&#x20;

You can view the number of Objects and fields selected for scanning in the top right corner.

<figure><img src="../../.gitbook/assets/image (1281).png" alt=""><figcaption></figcaption></figure>

Certainly! Here's a more concise version with grammatical accuracy and short sentences:

## **Apply Filters**

After selecting Salesforce Objects and Fields, you can refine your policy scope. Filters allow you to scan files owned or shared by specific users, groups, or profile members. You can also exclude files owned or shared by them.

Filters are optional. If you want to scan all users, groups, and profiles, you can skip this step.

To apply a filter, click **Add Filter** and select an option. Nightfall provides the following filters:

### **Internal Users**

Scan files owned or shared by specific internal users. You can also exclude files owned or shared by them.

### **Internal Groups**

Scan files owned or shared by specific internal groups. You can also exclude scanning of files owned or shared by members of internal groups.

**Note**: This filter cannot be used with the Salesforce Profiles filter.

### **Salesforce Profiles**

Scan files owned or shared by members with specific Salesforce profiles.&#x20;

**Note**: This filter cannot be used with the Internal Groups filter.







