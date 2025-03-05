---
description: >-
  Learn how to configure the scope section in Nightfall policies created for
  Microsoft OneDrive.
---

# Configure Scope for OneDrive

In this stage, you must select the tenant and the files of your OneDrive that must be monitored.&#x20;

To configure Scope, click **+ Add Tenant** and select a tenant.&#x20;

<figure><img src="../../../.gitbook/assets/image (927).png" alt=""><figcaption></figcaption></figure>

## Configuring the Inclusion Section

Once you select the tenant, you must select which drives in the selected tenant, must be monitored by Nightfall. This selection can be done in the **Include in monitoring** section.

<figure><img src="../../../.gitbook/assets/image (981).png" alt=""><figcaption></figcaption></figure>

### Selecting All Drives

To monitor all the drives in your OneDrive, you must select the **All OneDrives** option.&#x20;

### Configuring the Inclusion Section

<figure><img src="../../../.gitbook/assets/image (929).png" alt=""><figcaption></figcaption></figure>

#### Scan Documents with Permissions

Within your drives, files have different types of permission sets. Nightfall allows you to select files with specific permission types to be monitored. You can select the respective check box to monitor files with specific permission sets. To monitor all the files, irrespective of the permission, select **Access for all**.&#x20;

<figure><img src="../../../.gitbook/assets/image (930).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Check this [Microsoft document](https://support.microsoft.com/en-us/office/share-onedrive-files-and-folders-9fcc2f7d-de0c-4cec-93b0-a82024800c07) to learn more about file and folder permissions in OneDrive.&#x20;
{% endhint %}

#### Include Special Folders

In this section, you can select the special folders to be monitored. You can select the check box for the respective special folder to include it in monitoring. To select all the special folders, click **Select All**.&#x20;

<figure><img src="../../../.gitbook/assets/image (931).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Check this [Microsoft document](https://learn.microsoft.com/en-us/onedrive/developer/rest-api/resources/specialfolder?view=odsp-graph-online) to learn more about special folders in OneDrive.
{% endhint %}

### Selecting Specific Drives

To monitor drives specific to a user or group, you must select the **Selected OneDrives** option.&#x20;

<figure><img src="../../../.gitbook/assets/image (932).png" alt=""><figcaption></figcaption></figure>

Select the drives of the users and groups that must be monitored.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2024-04-23 at 4.00.15 PM.gif" alt=""><figcaption></figcaption></figure>

The [#scan-documents-with-permissions](scope.md#scan-documents-with-permissions "mention") and the [#include-special-folders](scope.md#include-special-folders "mention") configurations are the same as in case of [#selecting-all-drives](scope.md#selecting-all-drives "mention").

## Configuring the Exclusion Section

When you select the **All OneDrives** option, all the files and folders in your OneDrive are selected for monitoring. However, you can configure the exclusion section to skip some files and folders from being monitored. The exclusion section is optional and you can skip it if you wish to monitor all the drives. The exclusion section is not applicable if you select the **Selected OneDrives** option in the Inclusion section.

<figure><img src="../../../.gitbook/assets/image (982).png" alt=""><figcaption></figcaption></figure>

Nightfall provides you four options to configure the exclusion option.

### Exclude by OneDrives

In this option, you can directly select the individual or group OneDrives to be excluded from being scanned.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2024-05-02 at 10.26.30 AM.gif" alt=""><figcaption></figcaption></figure>

### Excluding By Label

In this option, you can select the labels to be excluded from being monitored. Currently, Nightfall supports only the sensitivity labels. Click [here](https://learn.microsoft.com/en-us/purview/sensitivity-labels) to learn more about the sensitivity labels. This option is in Beta because the Microsoft API used in this option is itself in Beta.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2024-05-02 at 10.31.21 AM.gif" alt=""><figcaption></figcaption></figure>

### Exclude by Folder Paths

In this option, you can enter the folder paths to be excluded. All the files and folders in the folder path are excluded from being scanned. The folder paths must be relative to the base of OneDrive.

<figure><img src="../../../.gitbook/assets/image (983).png" alt=""><figcaption></figcaption></figure>

The following points must be considered while using this option.

* All the input paths must begin with a forward slash (/).
* You cannot select only the root folder from exclusion. Basically, you cannot just include a forward slash in the **Folder paths** field. A valid folder path must follow the forward slash.
* You must specify the complete **Folder paths** field and end the folder path with a forward slash. If you enter /doc in the folder path, all the folders beginning with doc like /doc, /docs, /documents, doc1, and so on. To exclude only the doc folder, you must enter /doc/ in the **Folder paths** field.
*

### Exclude by File Extensions

In this option, you can select the file extensions. All the files with the selected extension are excluded from being scanned.&#x20;

<figure><img src="../../../.gitbook/assets/image (984).png" alt=""><figcaption></figcaption></figure>
