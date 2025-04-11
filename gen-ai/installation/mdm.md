---
description: >-
  Learn how to install the Nightfall DLP browser plugin across all devices of an
  organization.
---

# Install Nightfall DLP Across Organization

The steps in this document can only be performed by an Google Workspace admin user. The plugin is installed on all the user devices that are part of the Google Workspace. Google Workspace admins can install the plugin in two ways which are described as follows.

## Rollout Using MDM

Google Workspace administrators can use an MDM solution to rollout the extension across the chromium browsers.&#x20;

* [JAMF](https://learn.jamf.com/bundle/technical-paper-aws-verified-access/page/Downloading_and_Deploying_the_Manifest_File.html)
* [Kandji](https://support.kandji.io/support/solutions/articles/72000560463-google-chrome-management)
* [Chrome on Windows](https://support.google.com/chrome/a/answer/7532015?hl=en)
* [Edge on Windows](https://learn.microsoft.com/en-us/deployedge/microsoft-edge-manage-extensions-policies#force-install-an-extension)

## Rollout Using Chrome Management Google workspace

Google admin users can  use Google chrome, Firefox or any chromium browser to rollout the installation. The procedure remains the same. In this section, a Google Chrome browser is used.&#x20;

To rollout Chrome plugin using Chrome management:

1. Log in to your Google Workspace admin console.
2. Navigate to **Devices > Chrome > Apps & extensions**.
3. Click the **Users & browsers** tab.

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

4. Select the OU on which you wish to install the Nightfall DLP for browsers. By default, the top most level OU is selected.&#x20;

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

5. Hover the mouse on the **+** icon and select the **Add from Chrome Web Store** option.

<figure><img src="../../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

6. Search the term `Nightfall` in the search console and select **Nightfall DLP for Browsers**.&#x20;

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

7. Click **Select**.&#x20;

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

8. Click the **Installation policy** drop-down menu (by default, the **Allow install** option is selected in this drop-down menu).

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

9. Select the **Force install** option. (you can also select the **Fore install + pin to browser toolbar** option).

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

10. Click **SAVE**.

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

## Announce the Nightfall DLP Browser Installation

Once you have installed the Nightfall DLP browser, you can notify your organization of the benefits it can get them. You can educate them about the importance of using the extension in ChatGPT.
