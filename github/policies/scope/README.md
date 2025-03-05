---
description: >-
  Learn the process of configuring the Scope section while creating a Nightfall
  policy in Nightfall or GitHub.
---

# Configure Scope for GitHub

The Scope stage allows you to select a GitHub org in which you can the policy can be created.&#x20;

To configure Policy Scope:

1. Click **+ Org** and select the GitHub org.
2. Select one of the following options under the **Include in Monitoring** section. The scope of this policy is limited to only those repositories which you select in this section.&#x20;

* **All Repositories:** This option adds all the repositories (public and private) in your GitHub org to the policy scope.
* **Public Repositories:** This option adds all the public repositories in your GitHub org to the policy scope.
* **Private Repositories:** This option adds all the private repositories in your GitHub org to the policy scope.

{% hint style="info" %}
The **Total Monitoring Scope** section displays the number of GitHub repositories that will be monitored, based on your selection.
{% endhint %}



<figure><img src="../../../.gitbook/assets/GIF Recording 2023-10-31 at 11.11.24 AM.gif" alt=""><figcaption></figcaption></figure>

The **Exclude Repositories** section allows you to exclude repositories, files, and directories from the policy scope. It is optional and you can proceed without configuring this section, if you wish to maintain the scope of the policy to all the repositories and its directories, selected in Step 2.

3. Select a method to exclude repositories.&#x20;

* **Select Repository**: This option displays a drop-down menu of all the repositories selected in Step 2. You can directly select any repository to exclude it from the scope of the policy.
* **Enter pattern to exclude**: Select a text pattern to be matched for excluding repositories from policy scope.&#x20;
  * **Starts With**: All repositories that start with the mentioned text will be excluded.
  * **Ends With**: All repositories that end with the mentioned text will be excluded.
  * **Contains**: All repositories that contain the mentioned text will be excluded.
* **File Extension Exclusion**: Select a file extension. All the files with the selected extension are excluded from the policy scope.&#x20;
* **Directory Exclusion**: Enter a regular expression pattern to match a directory and file path. All file directories and file paths that match the pattern are excluded from the policy scope. All standard regular expressions are accepted, and you can refer to the documentation [here](https://github.com/google/re2/wiki/Syntax) for examples of regular expressions. You can also refer to [this link](https://regex-generator.olafneumann.org/?sampleText=2020-03-12T13%3A34%3A56.123Z%20INFO%20%20%5Borg.example.Class%5D%3A%20This%20is%20a%20%23simple%20%23logline%20containing%20a%20%27value%27.\&flags=i) to generate regular expressions.

{% hint style="info" %}
To learn more about how to use regular expressions to exclude GitHub directories, see [github\_regexp.md](github_regexp.md "mention").
{% endhint %}



<figure><img src="../../../.gitbook/assets/GIF Recording 2023-10-31 at 11.12.45 AM.gif" alt=""><figcaption></figcaption></figure>

4. Click **Next**.&#x20;

## Example Scenario

Consider that you wish to scan all public repositories of your GitHub account with Nightfall. However, there are a few public repositories that were created for testing purposes. These test repositories contain the word "test" in their names. You can use the **Repository Exclusion** drop-down menu to choose each repository that contains the word test. However, this task can be cumbersome.&#x20;

You can use the **Enter pattern to Exclude** menu with the Contains option and enter the term **test** in the field as shown in the following image.&#x20;

<figure><img src="../../../.gitbook/assets/GIF Recording 2023-12-08 at 3.44.13 PM.gif" alt=""><figcaption></figcaption></figure>

Consider another scenario in which you wish to include all the repositories but wish to exclude files with the "cert" extensions. You can accomplish this as shown in. the following image.

<figure><img src="../../../.gitbook/assets/GIF Recording 2023-12-08 at 4.06.01 PM.gif" alt=""><figcaption></figcaption></figure>
