---
description: >-
  Learn how you can use Microsoft Intune to install the Nightfall DLP for
  Browser
---

# Install Nightfall DLP with Microsoft Intune

This document explains the process of installing the Nightfall browser extension with Microsoft Intune. This deployment method is useful when you have organization level restrictions that prevent you from downloading the Nightfall browser extension from the Chrome web store.&#x20;

To install the Nightfall Browser Extension from Intune:

1. Log in to [Microsoft Intune](https://intune.microsoft.com/).
2. Navigate to the **Devices** section.
3. Click **Configuration**.

<p align="center"><img src="https://lh7-rt.googleusercontent.com/docsz/AD_4nXeJIjhoglBT4FRro51H5kUW_zwpYudVrv_6li0xOEB2RWdS8kwUBtg6QjVUWK1CFmMpOX_1Ab72CD8lqa1LJS3z2sp7_SDD8K0N5-p7cP3o_hyjOFAiWn4TgslB2gFZov-oOQTdWQ?key=QgohhY9UvOQTz24iG8yVlw" alt=""></p>

4. Select the **Windows** widget or the Windows option under the **Devices** menu.

<figure><img src="../../.gitbook/assets/image.png" alt="" width="563"><figcaption><p><br></p></figcaption></figure>

5. Click **Configuration**.
6. Click **+ Create** and select **+ New Policy**.
7. In the **Create a Profile** window select:
   1. **Windows 10 and Later** as the **Platform.**
   2. **Settings Catalog** as the **Profile Type**.
   3. Click **Create**.

<figure><img src="../../.gitbook/assets/image (1).png" alt="" width="375"><figcaption></figcaption></figure>

8. On the **Basics** tab:
   1. Enter a name for the policy
   2. (Optional) Enter a policy description.
   3. Click **Next.**

<figure><img src="../../.gitbook/assets/image (2).png" alt="" width="375"><figcaption></figcaption></figure>

9. On the **Configuration settings** tab, click **+ Add settings**.

<figure><img src="../../.gitbook/assets/image (3).png" alt="" width="563"><figcaption></figcaption></figure>

10. Search the extension keyword in the Settings picker search bar pane and select **Google Google Chrome Extensions**.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

11. Enable the Configure the list of Force-installed apps and extensions checkbox.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

12. Enable the **Configure the list of Force-installed apps and extensions** toggle button.

<figure><img src="../../.gitbook/assets/image (4).png" alt="" width="563"><figcaption></figcaption></figure>

13. Enter the following ID and click **Next**. This is the Nightfall browser extension ID obtained from the Google Chrome webstore.

```
jgmgecncmjklkabkejnjfgfkglapfgek
```

14. Click **Next**.

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

15. On the **Scope Tags** tab, click **Next**.
16. On the **Assignments** tab. Click **Add all users**.&#x20;
17. Click **Next**.

<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="563"><figcaption></figcaption></figure>

18. Review the configurations and click **Create**.

    \
    The Nightfall Chrome extension is installed automatically on each device once it logs in.

    \
