---
description: Learn how to operationalize NIghtfall Playbook.
---

# Playbook

## &#x20;💡 **Overview**

When implementing any new security tool or system, it is important to always consider the following for a seamless roll out:

1. Developing playbooks for the tool’s owners and primary users
2. Limiting disruption to end users
3. Maximizing impact and value of the tool

Nightfall is simple to implement all at once, but as with any tool, you want to make sure that you and your team are able to effectively incorporate a new tool into your day to day. This is especially important if you did not already have existing oversight into where sensitive information may have proliferated in your tech stack and you are going from 0 to 1 when it comes to discovering and managing violations.

To implement Nightfall effectively, we recommend a phased rollout - by tool coverage and by use case.

## **Steps**

### 1. Identify & prioritize tools & systems to protect with Nightfall

Which tools require imminent monitoring? Prioritize your systems accordingly.

We recommend phasing the rollout by tool or system simply because each new tool and system allows for different policy configurations. There is not a one-size-fits-all approach to remediating violations across tools and systems. Each tool will have its own “appropriate” measures for remediation based on what that tool’s function is at the company. For example, remediating violations on Slack can entail notifying, redacting, quarantining, or even deleting messages. However, those same actions do not apply in Google Drive; in Google Drive, Security teams care more about proper permissions and sharing settings. See below for considerations for each tool.

### 2. Identify & prioritize use cases

What are you solving for when monitoring tools for sensitive data? Are you fulfilling a compliance requirement? If so, which one(s)? Are you safeguarding secrets & credentials to protect customer data in your data warehouses?

Order these use cases in terms of priority.

By phasing the rollout by use case, you allow your team to thoughtfully consider the best practices for each use case so you can effectively train your end users. In addition, the phased rollout gives you an opportunity to assess the current state of affairs per use case without overwhelming your team with violations (in the event your end users are indeed sharing sensitive data inappropriately left and right — we hope not!).

### 3. Assess & update Security team responsibilities matrix, as needed. Designate owners

From a workflow perspective, consider how many SecOps team members will be managing violations. Larger teams may have multiple designated owners to manage violations for each product covered; smaller teams may only have a single designated owner to manage violations across all products. If you have a larger team, we recommend staffing coverage by product, as you can send alerts to separate channels to help optimize triaging. Additionally, each owner would be trained to handle and remediate violations across use cases, which allows for seamless team coverage in the event someone is out of the office.

Some teams like to designate ownership by use case. This is useful especially when there are cross-functional stakeholders involved and you want to align your Security team to functional teams. We would continue to recommend this approach so your business partners have a go-to partner on your team to oversee or manage joint security initiatives.

### 4. Start with your highest priority tool or system and use case

**i. Determine which teams and end users might be affected**

The teams and end users affected will vary depending on tool coverage and use case. Examples:

* Slack: likely to impact all employees
* Google Drive: likely to impact all employees
* GitHub: likely to impact the Engineering org
* Jira: likely to impact the Product and Engineering orgs; depending on which services in Jira your company uses, such as Jira Service Desk, this can also impact IT, Customer Success and Support, or even more broadly, the whole company
* Confluence: likely to impact all employees
* Salesforce: likely to impact the Go-To-Market org
* Zendesk: likely to impact Customer Success and Support teams
* Others: consider who are the primary users of the tool or system

**ii. Communicate with impacted teams and end users about Nightfall’s protection being in place**

[Template for rolling out Nightfall to your business users](coach_users.md)

**iii. Install Nightfall to cover the tool or system**

Please refer to our [Help Center](https://help.nightfall.ai/) or reach out to your CSM or [support@nightfall.ai](mailto:support@nightfall.ai) for additional support.

**iv. Identify scope of coverage within the tool or system**

Consider where you want to scan. This can vary product by product - in some cases, you will want to scan everywhere and everything; in others, in certain areas only. Review the [Considerations by Product](playbook.md#considerations-by-product) section for guidance.

**v. Set up your detectors, detection rules, and policies for your use case**

Review our [Detection Wizard](https://playground.nightfall.ai/detection-wizard) for details on how to set up your detection rules.

**vi. Monitor for 3-7 days to assess the lay of the land. Begin manually remediating findings**

Here are some initial [guiding principles on managing violations](https://help.nightfall.ai/operationalizing-dlp/guiding-principles). If you have a larger SecOps team managing violations per product, we strongly recommend following the third guiding principle. Acknowledging an alert helps to avoid duplicative efforts so that your team is spending their time efficiently.

**Ways to acknowledge an alert**

* If receiving alerts via Slack, put a reaction emoji on the alert to denote that you are looking on it, e.g. 👀 = “I have eyes on this”
* Use Nightfall’s in-alert `Acknowledge` action. The `Acknowledge` action can indicate that you have received the alert and are reviewing, or, if no other action needed, that the alert has already been reviewed

Some larger SecOps teams may also institute rotationals to manage alerts. These rotationals are much like on-call, where if you have multiple SecOps team members who might be reviewing alerts, you designate ownership in any given week to triage alerts. Each week, you would rotate who is responsible for reviewing violations. This accomplishes three things: clear ownership delineation per week, no single points of failure since multiple people will know how to manage alerts, and increased productivity across the team since people won’t be all jumping in to triage alerts at once.

For smaller teams, or teams where there is one individual responsible for managing alerts, we recommend time blocking 15 minutes at the beginning, middle, and/or end of the day on your calendar to review any outstanding violations. This helps eliminate context switching throughout the day and provides and ensures dedicated time to remediate any findings. The amount spent reviewing violations can and will be reduced over time as you institute automated remediation actions once ready.

#### **Ways to remediate a violation**

* Contact the end user: in general, we want the end user to understand the violation and what they should have done instead. For this reason, for every sensitive violation, we recommend reaching out to the end user to let them know of the violation and guide them towards best practices. [Template for flagging a violation to a user](coach_users.md). Note that when we set up notifications in the Nightfall platform, we can templatize this language for your company’s circumstances.
* Violation remediation is dependent on the product. Guides can be found within each integration page. For instance, you can find Slack remediation guide [here](https://help.nightfall.ai/nightfall-ai/nightfall-for-slack/slack-remediation-guide), GitHub remediation [here](https://help.nightfall.ai/nightfall-ai/nightfall-for-github/github-remediation-guide), and Google Drive remediation [here](https://help.nightfall.ai/nightfall-ai/nightfall-for-google-drive/nightfall-for-gdrive-manual-remediation).
* Test and sample data: test and sample data are often fine to be shared internally. To optimize your team’s bandwidth, we recommend no action needed on test and sample data. During step vii., we can fine tune out test and sample data, to reduce triggering violations on test and sample data as needed. You can find sample test data [here](https://help.nightfall.ai/nightfall-ai/nightfall-detection-and-policy-templates/nightfall-sample-data-sets).&#x20;

#### **Playbooking**

* As you get into the groove of managing violations, we strongly recommend documenting your processes. As your team grows, this playbook can become handy to ensure consistency in reviewing and remediating findings across your tech stack. Since remediation can ultimately differ by product and use case, writing down guidelines will help your team scale.

**vii. Tune and refine your detectors, detection rules, and policies**

As you learn new things about how your end users and other teams’ processes work, you can assess if those processes make sense from a security standpoint or adjust the configuration to accommodate. These are case by case situations and Nightfall can work with you to help identify what makes the most sense.

1. Detectors & detection rules: you may find that your company has specific identifiers, keywords, files, etc. that may trigger false positives. In this step, we can help refine these detectors and detection rules to ensure you are only receiving true positive alerts to manage. Nightfall also has a false positive annotation feature which will help train our detectors to improve for you over time.
2. Policies: during the process of monitoring violations with Nightfall, you will learn how other teams manage processes and you should work with your cross-functional business partner to determine what makes sense from a security standpoint. Nightfall is happy to join these conversations to support. In some cases, you may want to advise your business partner on process change management for their teams to ensure best security practices. In others, you may want to fit how the team remediates violations to their practices. E.g. a team is necessarily going to share files with sensitive data in Google Drive internally; you can ensure that they are not getting shared externally and refine policies to reflect this practice.

Nightfall will also automatically fine tune your detectors and detection rules to improve your configuration over time. However, the initial setup and fine tuning of your policies will set you up for long-term success.

**viii. Monitor for 3-7 days to assess impact**

You can review reporting and analytics on your [Nightfall dashboard](https://app.nightfall.ai).

**ix. Set up automated notification for the policy**

At this point, you should have a handle on the appropriate ways for users to share certain sensitive information with one another, if needed. In addition, your detectors and detection rules should be firing with a relatively high accuracy rate. Now is a good time to set up automated notifications on the policy because you can have confidence that Nightfall will notify and begin training your end users on alerts with accuracy.

Setting up automated notifications helps take one step off of your SecOps team’s plate. Before setting up this notification, we recommend creating an internal help center guide that the alert can point to for best practices. This helps with long-term training and documentation.

In the notification itself, you can point to this internal help center guide for further reading. Alternatively, if you prefer to not use a help center page, you can point your end users to different resources depending on the use case. For example:

* If you need to share secrets internally, please do so via \[1Password, Keybase, other encrypted tool, etc.].
* If you need to share sensitive PII internally, please do so using \[Keybase, other encrypted tool, etc.].
* If you need to share any of the above externally, please consult \[your manager] for guidance.
* If you have any questions, please feel free to reach out to Security at \[email address, Slack channel, etc.].

The goal of this notification is to guide end users towards the appropriate behavior so that over time your company adheres to the best security practices.

**x. If findings are highly sensitive, set up other automated actions as appropriate**

### 5. Repeat step 4 with next use case on the same tool or system, then with the next tool or system you want coverage for

Some habits will have already been built on workflows, but the introduction of a new use case may add nuance to how to manage violations from a different use case. For example, how you work with one team to share sensitive HR information with each other may be different from how you might address another team sharing secrets & credentials with one another.

Additionally, we recommend setting up separate Nightfall alert channels for each tool or system for ease of triaging violations.

## **Considerations by Product**

#### **Slack**

* Do you want to monitor shared channels? _Recommendation: we strongly recommend doing so because these are the channels where it is easiest for private data to be leaked into, even on accident_
* Do you want to monitor private channels and direct messages?

#### **Google Drive**

* Are there shared drives where sensitive data is allowed to be housed in? If so, who should have access to those drives? E.g. HR or Data team drives. _Recommendation: we strongly recommend continuing to monitor these drives but looking specifically for files where permission settings are too open, such as if those files are shared with anyone with the link, to external users, or even anyone in the organization. These files should remain on “Restricted” permission settings._
* Are there drives where data can be shared externally?

#### **GitHub**

* Are there private repos where sensitive data such as secrets & credentials are allowed to reside? _Recommendation: exclude these repos from scanning for those policies to limit noise._

#### **Jira**

* Are there any Jira Projects where you would expect and allow sensitive data to be shared? _Our view is that this is unlikely, but if so, you should exclude these from scanning._

#### **Confluence**

* Are there any Spaces or Pages where you would expect and allow sensitive data to be shared? _Our view is that this is unlikely, but if so, you should exclude these from scanning._

#### **Salesforce**

* Which objects or fields in your Salesforce instance are most likely to house sensitive information? Consider long text fields or objects where data may be synced from other sources (cases, activity history, attachments, emails, tasks).

#### **Zendesk**

* Are there any agents or groups of agents that are allowed to share sensitive information?
* If customers share sensitive information on accident, do you want that data removed immediately? _Recommendation: remediate findings on tickets that are in progress or closed, as sometimes your Customer Support agents need certain pieces of information to be effective. Once a ticket is closed, then that data should be removed immediately._
