---
description: Frequently Asked Questions for Nightfall DLP for Salesforce
---

# FAQs

#### How does Nightfall DLP for Salesforce leverage Salesforce Platform Events?

Nightfall DLP for Salesforce depends on the [Platform Events](https://developer.salesforce.com/docs/atlas.en-us.platform_events.meta/platform_events/platform_events_intro_emp.htm) messaging platform of a Salesforce org that Salesforce promotes as best practise to receive notifications for Salesforce events. Further, [Platform Events limits](https://developer.salesforce.com/docs/atlas.en-us.platform_events.meta/platform_events/platform_events_limits_default.htm) are shared across all workflows that leverage Platform Events and, per Salesforce, are replinished on a 24 hour rolling basis.

Every time an update happens on one of the objects monitoried by Nightfall DLP for Salesfoce, Nightfall's Salesforce package triggers an event that is queued in the Salesforce orgs Platform Events messaging queue. Subsequently Nightfall DLP Platform retrieves the event and the payload from the Platform Events queue and processes the update.

#### How Salesforce Platform Events limits affect Nightfall DLP for Salesforce processing?

Nightfall understands the criticality of Platform Events for Salesforce workflows and has defined a High Threshold and a Low Threshold for Platform Events usage on the customer's Salesforce org. If the Platform Events usage on the customer's Salesforce org breaches the High Threshold then Nightfall DLP for Salesforce will pause scan. Nightfall DLP for Salesforce will resume scan only when the Platform Events usage on the customer's Salesforce org goes below the Low Threshold. This way Nightfall DLP for Salesforce behaves as a model enterprise application and ensures that critical Salesforce workflows (like order processing) are prioritised over sensitive data scan.

Please reach out to your customer success manager for further details.

#### I selected Delete and Redact in my Policy. Is that a problem?

If you opted for both Redact and Delete actions in a policy for a set of objects and fields, Delete takes precedence over redact.&#x20;

All potential sensitive tokens are automatically deleted from the configured objects and fields.

#### On a single object, I want to configure a policy to automatically delete all credit card data, but auto-redact SSN.

You can create two policies on the object;

* one policy with a detection rule for the SSN detector, with redaction as the automated action.
* Another policy with a detection rule for credit card detector with delete as the automation action.

#### Why does Nightfall only scan emails that are sent, replied, forwarded but not the draft emails?

Salesforce may save emails in draft stage multiple times either because of the user action or automatically. Every save triggers a Salesforce event which causes Nightfall to scane the contents of the email draft if there is a policy to scan emails objects. This can lead to a situation where multiple violations are reported for the same sensitive data if the email is saved multiple times in the draft stage.&#x20;

So, Nightfall has disabled scanning of emails as long as they are in draft stage. However, emails will continue to be be scanned when other operations happen, for examples emails are sent, replied and forwarded. The user can reach out to Nightfall if they wish Nightfall to scan the drafts too, but it should be noted that as described above, this can lead to the same findings getting flagged across violations whenever the draft is saved.

#### Nightfall doesn’t remediate sensitive information from Email Message object. How do I solve this?

Email message is an immutable object in Salesforce. Therefore, Nightfall cannot modify the object record. You can delete the email from within Salesforce, once you receive a notification.

**I received a violation notification. However, the information was removed by the user in Salesforce. How will auto remediation respond?**

If the object does not contain sensitive information at the time of remediation, Nightfall will not remediate any data. Nightfall will re-scan the violated object and fields before performing any remediation.

#### I performed manual remediation on an object record after the object was deleted from Salesforce. How do I know if it was successful?

Nightfall detects that the object record does not exist anymore, and will stop remediation. A notification is sent to you.

#### How do I know if remediation action was successful?

Nightfall sends notifications for remediation action it performs.

#### A new version of the attachment was uploaded, can I remediate the previous version which had sensitive information?

No, Salesforce does not provide the option to delete specific versions of a file. Further, Salesforce only allows deletion of all the versions of an attachment. You can manually delete the attachment in Salesforce.

If the version was updated, and the object clears the scan, Nightfall will not delete the attachment and issues a notification with this information.&#x20;

#### If I have Einstein Activity Capture configured which synchronizes my mail and I see them in Salesforce. Can Nightfall detect sensitive information in these objects too?

No. Nightfall does not have the capability to detect sensitive information in any entity synced by Einstein Activity Capture.

#### What does the Nightfall DLP webhook notification for Salesforce look like?

Please see some example webhook responses below:

* Violations
* Manual Remediation
* Automated Remediation

#### Violation

```
{
"detectionRulesLink": "https://app.nightfall.ai/?intendedRoute=detection-engine/detection-rules",
"detectionRulesViolated": "SSN DR",
"eventType": "violation",
"message": "Policy violation detected in Salesforce",
"policiesLink": "https://app.nightfall.ai/?intendedRoute=salesforce/?policyUUID%5B%5D=cfa52d83-76d4-4840-a260-15e535c740a6",
"policiesViolated": "Account",
"service": "Salesforce",
"timestamp": "2022-06-22T06:34:30Z",
"violationID": "CRY7XI",
"violationMetadata": {
	"acknowledgeLink": "https://app.nightfall.ai/?intendedRoute=salesforce/remediation/082c0eb5-df1c-46cb-b8c2-f649747c9020/CRY7XI/acknowledge",
	"deleteRecordLink": "https://app.nightfall.ai/?intendedRoute=salesforce/remediation/082c0eb5-df1c-46cb-b8c2-f649747c9020/CRY7XI/delete",
	"event": "Record Updation",
	"fields": "description",
	"findingSnippets": [
		"SSN: 55*********."
	],
	"findings": "US social security number (SSN) (1 Very Likely)",
	"objectName": "Case",
	"orgName": "NightfallProdDemo",
	"orgType": "Sandbox",
	"recordID": "5008K000000yP86QAE",
	"recordLink": "https://prodnfdlpdemo--fullsandbo.sandbox.my.salesforce.com/5008K000000yP86QAE",
	"redactFindingsLink": "https://app.nightfall.ai/?intendedRoute=salesforce/remediation/082c0eb5-df1c-46cb-b8c2-f649747c9020/CRY7XI/redact",
	"who": "Mohit Mangnani",
	"whoLink": "https://prodnfdlpdemo--fullsandbo.sandbox.my.salesforce.com/0058a00000KgiirAAB"
},
"violationTime": "22 Jun 2022 at 6:34AM UTC"
}
```

#### Manual Remediation

```
{
	"eventType": "remediation",
	"message": "mohit+prod@nightfall.ai deleted finding(s).",
	"remediationMetadata": {
		"ActionUser": "mohit+prod@nightfall.ai",
		"actionType": "delete",
		"fields": "description",
		"objectName": "Case",
		"remediationType": "manual",
		"success": true,
		"unchangedFields": ""
	},
	"remediationTime": "22 Jun 2022 at 6:38AM UTC",
	"service": "Salesforce",
	"timestamp": "2022-06-22T06:38:07Z",
	"violationID": "CRY7XI"
}
```

#### Automated Remediation

```
{
	"eventType": "remediation",
	"message": "mohit+prod@nightfall.ai deleted finding(s).",
	"remediationMetadata": {
		"ActionUser": "mohit+prod@nightfall.ai",
		"actionType": "delete",
		"fields": "description",
		"objectName": "Case",
		"remediationType": "manual",
		"success": true,
		"unchangedFields": ""
	},
	"remediationTime": "22 Jun 2022 at 6:38AM UTC",
	"service": "Salesforce",
	"timestamp": "2022-06-22T06:38:07Z",
	"violationID": "CRY7XI"
}
```



