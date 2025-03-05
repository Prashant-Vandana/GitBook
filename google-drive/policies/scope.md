---
description: >-
  Learn how you can configure the Scope section in a policy, created in
  Nightfall for Google Drive.
---

# Configure Scope for Google Drive

The Scope stage allows you to include or exclude various Google drives, files, and folders from being monitored.&#x20;

The Scope stage consists of two main sections.&#x20;

* **Drive Selection**: This section allows you to include various files and drives for monitoring. In this section, you can select various drives to be monitored.&#x20;
* **Permission**: This section allows you to select files with specific permissions, shared with any internal or external users or user groups.
* **Add Filters**: This section allows you to scrutinize your policy scope at more granular levels. While the Permission section allows you to select all the files belonging to a specific permission type and all the internal or external users and groups, in this section you can add filters to include or exclude individual files, users, and groups from being monitored or being excluded from monitoring.

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

## Configuring the Drive Selection Section

The **Drive Selection** section allows you to select various drives for monitoring. You can select either User Drives or Shared drives to be monitored by Nightfall for sensitive data.&#x20;

<figure><img src="../../.gitbook/assets/image (1057).png" alt=""><figcaption></figcaption></figure>

### Select Drives

This section allows you to select various drives in your Google Drive to be monitored. There are two options in this section. You can either choose to scan the User drives, Shared drives, or both.&#x20;

* **User Drives**: The User Drives is the personal drive of the user. The files in this drive are visible only to the owner of the file and other users to whom the owner has given access. User Drive is commonly known as **My Drive** in Google Drive. To select the User drive for scanning, you must select the **User drives** check box.

{% hint style="success" %}
**IMPORTANT**

If you choose to monitor the User drives, all the User drives in your Google domain are selected for monitoring. You do not have the option to choose specific User drives for monitoring.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (1058).png" alt=""><figcaption></figcaption></figure>

* **Shared Drives**: Shared drives are common storage locations accessed by all the users in your organization. To select this option, you must select the **Shared drives** check box.

{% hint style="success" %}
**IMPORTANT**

If you choose to monitor the Shared drives, you can select whether to monitor all the Shared drives or only specific shared drives. &#x20;

* &#x20;If you select the **All Drives** option, all the Shared drives in your Google domains are selected for monitoring.
* If you select the **All Drives, except for** option, you can exclude some shared drives from being monitored.
* If you select the **Specific Shared Drives** option, you get the option to choose specific Shared drives for monitoring.&#x20;
{% endhint %}

The following image displays the scenario when you select the **All Shared drives** check box.&#x20;

<figure><img src="../../.gitbook/assets/image (1059).png" alt=""><figcaption></figcaption></figure>

If you select the **All Drives, except for** option, you must also select the shared drives which must be excluded from monitoring.&#x20;

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

Similarly, if you select the **Specific Drive(s)** option, you must also select the specific shared drives which must be monitored.

## Configuring the Permission Section

The Permission section allows you to add all the files, users, and user groups that match a certain criteria, to the scope of the policy. This section has the following configurations.

* [General Access](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#heading=h.joh558i114zh)
* [Shared With](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#heading=h.qaydu0gor221)

{% hint style="info" %}
If you wish to scan all the files in the selected drive(s), you can skip this section.&#x20;
{% endhint %}

### General Access

The general access feature in Google Workspace consists of three types of access, which are as follows.&#x20;

* **Restricted**: Files with this permission can only be accessed by users or groups who have been granted direct access.
* **Target Audience**: Files with this permission can be accessed by the users of the selected target audience group. There is a default target audience that gets created when the Google workspace is provisioned. This target audience has the same name as provisioned in the Google Workspace and includes all members of the organization. You can refer to this [Google document](https://support.google.com/a/answer/9934697?hl=en) to learn more about the target audiences.&#x20;
* **Anyone with the Link**: Files with this permission can be accessed by any user who has the file link.

<figure><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXefdzzbO5ZmxB4WmZ7BKrDPujTwPLs5P7VEcQy8wVRncGmxrKPX94pCzla92TDAqP_SITTmjo_xo7sDhXps4zI2LQYjPsv_RDNvym7AVhrXAVuPQr8H5qxuSOQazzyZvoBriCXUHnvToTxLUAwmf7c6VlEU?key=rKlAFIVj-I0RxOBt9z11lw" alt="" width="563"><figcaption></figcaption></figure>

The Nightfall **General Access** permission options map 1x1 to the General Access sharing principle in Google Workspace.

<figure><img src="../../.gitbook/assets/image (657).png" alt=""><figcaption></figcaption></figure>

* **Restricted**: If you select this option, all the files from within the selected drive (User Drive or Shared Drive) which have the Restricted permission are monitored by the policy.&#x20;
* **Shared with target audiences**: If you select this option, all the files from within the selected drive (User Drive or Shared Drive), which have general access set to any of the target audiences, are monitored by the policy.&#x20;
* **Anyone with the link**: If you select this option, all the files from within the selected drive (User Drive or Shared Drive), which have the Anyone with the Link permission are monitored by the policy.&#x20;

### Shared With

The **Shared With** section allows you to select the files which are directly shared with any internal users/groups and any external users/groups.

<figure><img src="../../.gitbook/assets/image (658).png" alt=""><figcaption></figcaption></figure>

* **Internal users or groups**: If you select this option, all the files which are accessible by any internal user(s) or internal group(s) via direct access (not via link or target audience), are monitored by the policy.
* **External users or groups**: If you select this option, all the files which are accessible by any external user(s) or external group(s) via direct access (not via link or target audience), are monitored by the policy.

For instance, let’s assume that Acme corp has 10 external users. They select the **External users or groups** option. Now, even if one of the 10 external users has direct access to a file, it will be monitored by the policy. In this case, only if a file is not shared with any of the 10 external users, the file will be excluded from being monitored.

{% hint style="info" %}
Nightfall does not check the membership details for external groups.
{% endhint %}

## Configuring Add Filter Section&#x20;

The filters section provides you the flexibility to include and exclude users at a granular level.&#x20;

For instance, in the previous section under the **Shared With** section, if you select the **Internal users or groups** option, all the internal users and groups are selected. You cannot filter and pick specific individual internal users or groups to include or exclude from being monitored or excluded. This flexibility can be leveraged by using the **Add Filter** section. Nightfall allows you to use filters on the following entities.

[Internal Users](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#heading=h.4fit8czf16e)

[External users](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#heading=h.c183oac3fzpa)

[Internal Groups](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#bookmark=id.ly3otse9lvbh)

[External Groups](https://docs.google.com/document/d/1BA-XCcxwsLPh5oC5aT4pRDY9oqHpo89F9-I7SGJP6uY/edit#bookmark=id.imghuhwqnsga)

[Labels](https://help.nightfall.ai/sensitive-data-protection/google-drive/policies/scope#labels)

[Domains](https://help.nightfall.ai/sensitive-data-protection/google-drive/policies/scope#domains)

[Files](https://help.nightfall.ai/sensitive-data-protection/google-drive/policies/scope#files)

### Internal Users

* **Specific User(s)**: You must choose this option to monitor files that are owned by or accessible to specific internal users. Once you choose this option, Nightfall populates the list of users from the synced IdPs in [directory\_sync](../../nightfall_settings/directory_sync/ "mention"). You must select the required users. &#x20;
* **All Users, except for**: You must select this option to exclude files which are owned by or accessible to specific internal users. Once you choose this option, Nightfall populates the list of users from the synced IdPs in [directory\_sync](../../nightfall_settings/directory_sync/ "mention"). You must select the required users.

<figure><img src="../../.gitbook/assets/image (1278).png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
**Note**&#x20;

If you have not configured the [Directory Sync](https://help.nightfall.ai/nightfall-ai/nightfall-settings/directory-sync) feature, the users list is populated from the [Google Drive integration setup](https://help.nightfall.ai/nightfall-ai/nightfall-for-google-drive/installation-instructions-nightfall-for-google-drive/installing-nightfall-for-google-drive). As a result, you can see the Google Drive icon before the user name. However, if you have set up Directory sync, the users list is fetched from the IdP used for the configuration. In the above image, the users list is populated from the Microsoft Azure IdP and hence you can see the Azure icon before the users’ names.
{% endhint %}

{% hint style="info" %}
**Important**

For exclusions, Nightfall only checks the file ownership (\*Nightfall also checks for shared access, but for exclusion to work for shared access, no user or group that is otherwise included should have access to the file, for it to be considered excluded). For inclusions, Nightfall checks both file ownership and shared access. This rule is applicable to all the filters.
{% endhint %}

**Example Scenario**

For instance, let’s assume that Acme corp has 4 users who are part of Acme’s Google Workspace. The four users are Tom, Rick, Harry, and Steve. All four users have access to a file. Acme corp wishes to scan only those files which are owned or accessed only by Harry and Steve. They select the Internal users or groups option under the Shared With section. They apply the Internal Users filter, set the filter as Monitor specific and select Harry and Steve. Now only those files which are owned or accessible to either Harry, Steve, or both, are monitored by the policy.

### External Users

* **Specific User(s)**: You must choose this option to monitor files that are accessible to specific external users. Once you choose this option, you must manually type the email ID of the required users and hit the enter key.
* **All Users, except for**: You must choose this option to exclude files which are accessible by specific external users, from being monitored. Once you choose this option, you must manually type the email ID of the required users and hit the enter key.

**Example Scenario**

For instance, let’s assume that Acme corp has 4 users who are external to Acme’s Google Workspace. The four users are **Tom, Rick, Harry**, and **Steve**. All four users have access to a file. Acme corp wishes to scan only those files which are accessed only by **Harry** and **Steve**. They select the **External users or groups** option under the **Shared With** section. They apply **External Users** filter, set the filter as **Monitor specific** and select **Harry** and **Steve**. Now only those files which are accessible to either Harry, Steve, or both, are monitored by the policy.

### Internal Groups

* **Specific Group(s)**: You must choose this option to monitor files that are accessible to specific internal groups. Once you choose this option, Nightfall populates the list of internal groups from the synced IdPs in [directory\_sync](../../nightfall_settings/directory_sync/ "mention"). You must select the required users.&#x20;
* **All Groups, except for**: You must choose this option to exclude files which are accessible by specific internal groups, from being monitored. Once you choose this option, Nightfall populates the list of internal groups from the synced IdPs in [directory\_sync](../../nightfall_settings/directory_sync/ "mention"). You must select the required users.&#x20;

**Example Scenario**

For instance, let’s assume that Acme corp has three internal groups. The three groups are **Development**, **Testing**, and **Customer Success**. Acme Corp wishes to scan only those files accessed by the **Customer Success** group since the users of this group interact with customers and Acme does not wish them to leak any file with sensitive data to customers. Acme Corp selects the **Internal users or groups** option under the **Shared With** section. They apply the **Internal Groups** filter, set the filter as **Monitor specific** and select **Customer Success**. Now only those files which are accessible to the group email ID of Customer Success, are monitored by the policy.

### External Groups

* **Specific Group(s)**: You must choose this option to monitor files that are accessible to specific external groups.&#x20;
* **All Groups, except for:** You must choose this option to exclude files which are accessible by specific external groups from being monitored.

**Example Scenario**

For instance, let’s assume that Acme corp has three external groups. The three groups are **Sales**, **Marketing**, and **Customer Success**. Acme Corp wishes to scan only those files accessed by the **Customer Success** group. Acme Corp selects the **External users or groups** option under the **Shared With** section. They apply **External Groups** filter, set the filter as **Monitor specific** and select **Customer Success**. Now only those files which are accessible to the group email ID of Customer Success, are monitored by the policy.

{% hint style="warning" %}
**Important**

If you have not configured Directory sync, in case of internal and external groups, Nightfall can only compare the entered group mail ID with the email ID of the group, and cannot check for the members of the groups. To check group membership, you must configure Directory Sync. Without Directory sync configured, if you enter a group mail ID, Nightfall does not display the number of users who are part of the group.
{% endhint %}

### Labels

A Label is a metadata that you can create to help users organize, find, and apply policy to files in Google Drive. To learn more about Google Drive Labels, refer to this [Google document](https://developers.google.com/drive/api/guides/about-labels).&#x20;

{% hint style="warning" %}
Before utilizing filters for Labels, you must [enable Google Drive Labels](https://help.nightfall.ai/nightfall-ai/nightfall-for-google-drive/installation-instructions-nightfall-for-google-drive/enabling-google-drive-labels) as per instructions and create labels in your Google Drive.&#x20;
{% endhint %}

You can choose one of the following options.&#x20;

* **Specific Label(s)**: You must choose this option to monitor only those files that contain the selected Labels. Once you choose this option, you must select the Labels. Nightfall only monitors those files that have the selected labels.
* **All Labels, except for**: You must choose this option to exclude the monitoring of files that contain the selected Labels. Once you choose this option, you must select the Labels. Nightfall does not monitor the files that contain the selected labels.

### Domains

A Domain typically refers to an organization's email domain or Google Workspace domain. You can configure Nightfall to monitor specific domains or exclude certain domains from monitoring. &#x20;

* **Specific Domain(s)**: Nightfall will only monitor files associated with the specified domains. You can choose the option to monitor files that have been shared with specific domains. Once you choose this option, you must manually enter the domain (for example, abcd.com) and hit the enter key. Nightfall only monitors those files that belong to the selected domains.

{% hint style="success" %}
To include personal email domains (e.g., gmail.com, yahoo.com), check the "Add free personal email domains" box. This automatically includes files shared with common personal email services such as gmail.com, yahoo.com, etc for scanning.
{% endhint %}

* **All Domains, except for**: You must choose this option to exclude the monitoring of files that are shared with the selected domains. Once you choose this option, you must manually enter the domain (for example, abcd.com) and hit the enter key. Nightfall does not monitor those files that belong to the selected domains.

### Files

You can choose to monitor or exclude monitoring of specific files. To include or exclude files for monitoring, you must enter the file ID of the required file(s). You can find the File ID of a Google Drive file from the file URL. The format is as follows.

```http
https://docs.google.com/[documents]/d/[file ID]/…
```

* **Specific Files(s):** You must choose this option to monitor only the selected files. Once you choose this option, you must manually enter the file ID of the file and hit the enter key. Nightfall only monitors those files whose IDs are entered here. No other filters are evaluated if this filter is configured and only the selected files are scanned.
* **All Files, except for**: You must choose this option to exclude the monitoring of specific files. Once you choose this option, you must manually enter the file ID of the file and hit the enter key. Nightfall does not monitor those files whose IDs are entered here.

## Conflict Management

When setting up Google Drive policies, you can include or exclude specific users, user groups, and drives. Users and groups are synced via Okta, Entra, or Google directory. Here's how Nightfall resolves conflicts across configured filters in a sensitive data protection policy for Google Drive:

### **1. Drive Filters**

* **Drive Inclusions**: Specify drives to be scanned in this policy.
* **Drive Exclusions**: Specify drives to be exempt from scanning in this policy.

### **2. General Access** Filters

**a. If no options are selected in this filter**:

* No files will be automatically included for scanning based solely on their general access settings.
* Files may still be scanned based on other filter criteria in the policy.
* The policy will rely on other configured filters to determine which files should be scanned. At least one of the options in general access filters or shared with filters need to be selected for any files to be scanned via a policy.&#x20;

**b. Options:**&#x20;

* "Restricted": Files with this setting are included for further filtering.
* "Shared with target audience": Files with ANY target audience setting are included for further filtering.
* "Anyone with link": Files with this setting are included for further filtering.

### **3. Shared With** Filters

&#x20;       **a. If no options are selected in this filter**:

* Files that are shared directly with ANY user or user groups will be ineligible for scanning specifically for this check.
* Files that are not shared at all may still be eligible for scanning based on other filter criteria.
* The policy will rely on other configured filters to determine which files should be scanned.
* The policy will rely on other configured filters to determine which files should be scanned. At least one of the options in general access filters or shared with filters needs to be selected for any files to be scanned via a policy.

&#x20;      **b. Options**:

* **Internal users or groups**: Files not shared directly with ANY internal user or group are ineligible for scanning specifically for this check.
* **External users or groups**: Files not shared directly with ANY external user or group are ineligible for scanning specifically for this check.

### 4. File Filters

* **File Inclusions**: If left unconfigured, all files are included for further filtering. When specific files are listed, they are always scanned and all other filters are ignored.&#x20;
* **File Exclusions**: If left unconfigured, no files are automatically excluded. Listed files are never scanned under this policy.

{% hint style="success" %}
Files can be included or excluded by specifying the file ID. File IDs can be found directly in their URL. The format is https://docs.google.com/\[documents]/d/\[file ID]/…
{% endhint %}

### 5. Label Filters

1. **Label Inclusions**: If left unconfigured, labels on files are not evaluated for inclusions. When specific labels are listed, only files with these labels are scanned for this specific policy check.
2. **Label Exclusions**: If left unconfigured, labels on files are not evaluated for automatic exclusion of files. Files with listed labels are ineligible for scanning specifically for this policy check.

### **6. User Filters**

* **User Inclusions**: If left unconfigured, all users are included. For listed internal users, files neither owned nor shared with them are ineligible for this specific check. For listed external users, files not shared with them are ineligible for this specific check.
* **User Exclusions**: If left unconfigured, no users are automatically excluded. For listed internal users, files they own or are ONLY accessible by them are ineligible for this specific check. For listed external users, files ONLY accessible by them are ineligible for this specific check.

### **7. Group Filters**

* **Group Inclusions**: If left unconfigured, all groups are included. For listed internal groups, files neither owned nor shared with any member of these groups are ineligible for this scan. For listed external groups, files neither owned nor shared with the external group email are ineligible for this scan.
* **Group Exclusions**: If left unconfigured, no groups are automatically excluded.

### 8. Domain Filters

* **Domain Inclusions**: If left unconfigured, all domains are included. For listed domains, files neither owned nor shared with at least one user belonging to the specified domains are not eligible to be scanned.
* **Domain Exclusions**: If left unconfigured, no domains are automatically excluded. For listed domains, files owned or shared only with users belonging to the specified domains are eligible to be excluded from scanning.

