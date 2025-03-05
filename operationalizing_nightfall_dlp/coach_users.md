---
description: Learn the process of informing and teaching users about Nightfall platform.
---

# Informing & Coaching Business Users

Cloud security is a team sport, and we recommend that you work within your broader organization to achieve understanding and buy-in for a successful DLP program.

Your organization’s users play a large role in keeping your organization safe from a DLP perspective - after all, they are the ones who are interacting with cloud applications to create and edit information every day. We recommend communicating with your broader organization during the early phases of implementing your new cloud DLP approach, so users are not caught off guard if they are involved in a violation that requires remediation. Transparent communication up front can go a long way toward mitigating users’ feelings of being “monitored” or “reprimanded.” See below for a template message you can send out company-wide.

**Template for rolling out Nightfall to your business users:**

> Hi all,
>
> **\[PRODUCT NAME: Slack, Google Drive, GitHub, Confluence, Jira]** are integral to how we work together at **\[Company Name]**. Many of us use **\[Product Name]** regularly to collaborate and to be effective in our day to day work.
>
> As **\[Company Name]** continues to grow, it remains critically important to protect and secure the information that we share within and across products. Starting **\[Roll out date]**, we will begin using a data loss prevention tool called Nightfall which will monitor **\[Product Name]** so that sensitive data (e.g. customer PII, employee personal data, or other forms of restricted data) is not shared or stored insecurely.
>
> **Why is this important?**
>
> Our customers require us to provide a high level of protection for any data that they provide to **\[Company Name]**. When we share sensitive data, it should be through a secure cloud sharing solution and not across cloud applications that are not intended to house sensitive information.
>
> **What is sensitive or restricted data?**
>
> Sensitive or restricted data is a classification of information at **\[Company Name]**. This data is often customer or employee personal data, including SSNs, credit card information, dates of birth, and credentials.
>
> **How does this impact you?**
>
> If you have access to sensitive or restricted data, please be mindful of where and with whom you share it in **\[Product Name]**. Note that our security team may reach out to you to help with remediating any violations to ensure that our data is safe and secure.
>
> If you have any questions, please reach out to **\[Security Team email]**. Thanks for helping to keep **\[Company Name]** secure!

We also recommend that you work closely with users as violations materialize, and take the opportunity to educate them or even involve them in remediation efforts. The end goal should be to reduce violations from occurring in the first place, with the DLP program functioning as a safeguard in case of slip ups. Coaching and education are the true foundations to reduce DLP violation occurrences, and by empowering end users to be active participants, you can also reduce some of the follow up actions needed from your team.

There are two aspects to this:

1. Real-time training as violations arise
2. Regular best practices training and content

When violations come up, the best practice is to contact the user upon review and let them know that the sensitive information was flagged and ask them to remediate the violation for the company’s security.

**Template for flagging a violation to a user:**

{% tabs %}
{% tab title="Slack Violations" %}
_Note: if you are using the Slack product, there is a built-in template that will send a message to users if you select the “Notify User” remediation option. This template can be customized in the_ [_Nightfall dashboard_](https://app.nightfall.ai/)_._

Hi **\[Name]**,

We noticed you shared content that may contain sensitive information in Slack at this link: **\[insert link]**. Did you intend to send this message? If not, could you please delete it? We would like to ensure security best practices to ensure **\[Company Name]** has the strongest security posture for our data.

Thanks!&#x20;
{% endtab %}

{% tab title="Google Drive Violations" %}
Hi **\[Name]**,

We noticed this file you shared **\[externally]** in Google Drive may contain sensitive information: **\[insert link]**. Did you intend to share this with the external parties? If not, can you help adjust the sharing settings to be "Restricted" or to "Users in our organization only"? We would like to ensure security best practices to ensure **\[Company Name]** has the strongest security posture for our data.

Thanks!&#x20;
{% endtab %}
{% endtabs %}

To communicate best practices more broadly, we would recommend reviewing the top violations found by Nightfall and identifying the best way for users to resolve or avoid those violations.

**Template for communicating best practices to the company:**

> Hi all,
>
> A few weeks ago, the Security team implemented a data loss protection tool called Nightfall, which detects sensitive information shared between users on **\[Product]**.
>
> To date, Nightfall has scanned **\[XXX]** messages that detected sensitive information not authorized for sharing via **\[Product]**. This baseline data highlights a few trends that violate our security policies.
>
> We’d like to remind everyone to follow the below security protocols and secure sharing practices:
>
> * Customer PII and employee personal data should never be shared over **\[Product]**.
> * **\[insert key security protocols and best practices for sharing at your company; examples below]**
> * _Example: Passwords of any kind must be stored in \[1Password/LastPass/RPass] or another secure password vault._
> * _Example: Passwords should be complex and unique. Use \[1Password/LastPass/RPass]’s password generator to generate random string passwords - not “Acme123!” or passwords without sufficient randomness._
> * _Example: Passwords should never be posted in a shared document._
> * _Example: API Authentication tokens (e.g., Basic, Bearer) or Private Keys are effectively passwords and should never be stored or sent in plain text._&#x20;
>
> If you are aware of sensitive information that could be mishandled, or you’d like help share sensitive information in a safe and secure way, please reach out to **\[security@acme.com]**.
>
> Thank you for always keeping **\[Company Name]** secure!&#x20;
