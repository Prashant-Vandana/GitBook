# Table of contents

* [Welcome to Nightfall Documentation](README.md)

## Release Notes <a href="#release_notes" id="release_notes"></a>

* [Release Notes 2025](release_notes/nightfall_new_features.md)
* [Release Notes 2021-2024](release_notes/release_notes_old.md)

## Introduction <a href="#nightfall_introduction" id="nightfall_introduction"></a>

* [Why Cloud DLP?](nightfall_introduction/cloud_dlp.md)
* [Introduction to Nightfall](nightfall_introduction/nightfall_overview.md)
* [Nightfall Overview](nightfall_introduction/overview.md)
* [Cloud-native DLP vs. CASB](nightfall_introduction/cloud_dlp_casb.md)
* [How Nightfall Works](nightfall_introduction/overview_nightfall.md)
* [Reasons to Choose Nightfall](nightfall_introduction/why_choose_nightfall.md)
* [Benefits of Nightfall](nightfall_introduction/benefits.md)

## Compliance <a href="#nightfall_compliance" id="nightfall_compliance"></a>

* [How Nightfall Fits into Compliance Frameworks](nightfall_compliance/compliance_with_nightfall.md)
* [ISO 27001 Compliance + DLP](nightfall_compliance/iso-27001.md)
* [SOC 2 Compliance + DLP](nightfall_compliance/soc2.md)
* [PCI Compliance + DLP](nightfall_compliance/pci.md)
* [PHI Detector - More on Nightfall's HIPAA Compliance Detector](nightfall_compliance/phi_hipaa.md)

## Getting Started <a href="#get_started" id="get_started"></a>

* [Installing Nightfall](get_started/installation.md)

## Nightfall Detection Platform <a href="#detection_platform" id="detection_platform"></a>

* [Overview](detection_platform/overview.md)
* [Detectors](detection_platform/detectors.md)
* [Choosing a Nightfall Detector](detection_platform/choosing_detectors/README.md)
  * [Compliance Use Cases](detection_platform/choosing_detectors/compliance_use_cases.md)
  * [Data Protection Use Cases](detection_platform/choosing_detectors/data_protection_use_cases.md)
* [Nightfall Detector Glossary](detection_platform/detection_glossary/README.md)
  * [Secrets Detection](detection_platform/detection_glossary/secrets_detection.md)
* [Creating Custom Detectors](detection_platform/custom_detectors/README.md)
  * [Creating Dictionary Detector](detection_platform/custom_detectors/dictionary_detector.md)
  * [Create File Type Detector](detection_platform/custom_detectors/file_type_detector.md)
  * [Create File Fingerprint Detector](detection_platform/custom_detectors/file_fingerprint_detector.md)
  * [Create Regular Expression Detector](detection_platform/custom_detectors/regexp_detector.md)
  * [Extend a Nightfall Detector](detection_platform/custom_detectors/extend_nightfall_detector.md)
* [Create Detection Rules](detection_platform/create_detection_rules.md)
* [Detection Platform Overview](detection_platform/overview_platform.md)
* [Evaluating Detection](detection_platform/evaluate_nightfall_detection.md)
* [Creating Policies](detection_platform/policies/README.md)
  * [Selecting Integration](detection_platform/policies/integration.md)
  * [Scope of the Policy](detection_platform/policies/scope.md)
  * [Detection Rules](detection_platform/policies/detection_rules.md)
  * [Advanced Settings](detection_platform/policies/advanced_settings.md)
  * [Name and Risk Score](detection_platform/policies/risk_score.md)
* [Historical Scan Detection Rules](detection_platform/historical_scan.md)
* [Regex Library](detection_platform/regex_library.md)
* [Detection Platform FAQs](detection_platform/faq/README.md)
  * [How can I reduce false positives in my findings?](detection_platform/faq/reduce_false_positives.md)
  * [What do different “Confidence Levels” mean?](detection_platform/faq/confidence_levels.md)
  * [What file types will Nightfall scan for sensitive data? What are the limitations?](detection_platform/faq/file_types_scanned.md)
  * [How do I use Context Rules?](detection_platform/faq/context_rules.md)
  * [How do I use Exclusion Rules?](detection_platform/faq/exclusion_rules.md)
  * [Does Nightfall have a regex library I can choose from?](detection_platform/faq/regex_library.md)
  * [Why does Nightfall sometimes miss to report SSN, credit card number, and so on?](detection_platform/faq/report_ssn.md)
  * [Why does the Password Detector Report False Positive Zoom Password Findings?](detection_platform/faq/false_positive.md)

## Nightfall Detection & Policy Templates <a href="#nightfall_policy_templates" id="nightfall_policy_templates"></a>

* [Detection Rules](nightfall_policy_templates/detection_rules.md)
* [Nightfall Sample Data Sets](nightfall_policy_templates/sample_data.md)

## Dashboard and Events <a href="#dashboard" id="dashboard"></a>

* [Nightfall Dashboard](dashboard/overview.md)
* [Data Detection and Response Events](dashboard/sdp_events/README.md)
  * [Filtering Events](dashboard/sdp_events/filtering.md)
  * [Event Filter Operators](dashboard/sdp_events/filter_operators.md)
  * [Applying Actions on Events](dashboard/sdp_events/event_actions.md)
  * [Applying Bulk Actions on Events](dashboard/sdp_events/bulk_actions.md)
  * [Event Status](dashboard/sdp_events/status.md)
  * [Deduplication and Automatic Resolution of Events](dashboard/sdp_events/deduplication.md)

## Setting up Alert Platforms <a href="#nightfall_alert_platform" id="nightfall_alert_platform"></a>

* [Nightfall Alert Platforms](nightfall_alert_platform/overview.md)
* [Setting up Slack as an Alert Platform](nightfall_alert_platform/alerting_to_slack.md)
* [Setting up Jira as an Alert Platform](nightfall_alert_platform/alerting_to_jira.md)
* [Setting up MS Teams as an Alert Platform](nightfall_alert_platform/alerting_to_ms_teams.md)

## Operationalizing Nightfall DLP <a href="#operationalizing_nightfall_dlp" id="operationalizing_nightfall_dlp"></a>

* [Playbook](operationalizing_nightfall_dlp/playbook.md)
* [Informing & Coaching Business Users](operationalizing_nightfall_dlp/coach_users.md)
* [Alert Management Guiding Principles](operationalizing_nightfall_dlp/alert_guiding_principles.md)
* [Integrating with Security Tools](operationalizing_nightfall_dlp/security_tools_integration/README.md)
  * [Integrating with SIEM](operationalizing_nightfall_dlp/security_tools_integration/siem/README.md)
    * [Integrating with Microsoft Sentinel](operationalizing_nightfall_dlp/security_tools_integration/siem/microsoft_sentinel.md)
  * [Creating Dashboards for Nightfall Alerts in Splunk](operationalizing_nightfall_dlp/security_tools_integration/splunk.md)
  * [Creating Dashboards for Nightfall Alerts in Sumo Logic](operationalizing_nightfall_dlp/security_tools_integration/sumo_logic.md)
  * [Sending Alerts to Microsoft Teams](operationalizing_nightfall_dlp/security_tools_integration/ms_teams.md)
* [Frequently Asked Questions (FAQs) for End-Users](operationalizing_nightfall_dlp/faqs_end_users.md)

***

* [Nightfall Integrations](nightfall_integrations.md)

## Nightfall for Slack <a href="#slack" id="slack"></a>

* [Nightfall for Slack: Quick Start](slack/quickstart.md)
* [Getting Started With Nightfall for Slack](slack/getting_started/README.md)
  * [Requirements](slack/getting_started/requirements/README.md)
    * [Requirements for Nightfall DLP for Slack Enterprise](slack/getting_started/requirements/slack_enterprise.md)
    * [Requirements for Nightfall DLP for Slack Pro and Slack Business+](slack/getting_started/requirements/slack_pro.md)
  * [Installing Nightfall for Slack](slack/getting_started/install/README.md)
    * [Installing Nightfall DLP for Slack Enterprise](slack/getting_started/install/slack_enterprise.md)
    * [Installing Nightfall DLP for Slack Pro and Business+](slack/getting_started/install/slack_pro.md)
* [Configure Alerts for Slack](slack/integration_alerts.md)
* [Configuring Policies for Slack Pro and the Slack Business+ Editions](slack/slack_pro_policy/README.md)
  * [Slack Pro and Business+ App Selection](slack/slack_pro_policy/integration.md)
  * [Configure Scope for Slack Pro and Slack Business+](slack/slack_pro_policy/scope.md)
  * [Configure Detection Rules for Slack Pro and Slack Business+](slack/slack_pro_policy/detection_rules.md)
  * [Configure Automated Actions in Slack Pro and Slack Business+](slack/slack_pro_policy/automated_actions.md)
  * [Configure Advanced Settings in Slack Pro and Slack Business+](slack/slack_pro_policy/advanced_settings.md)
  * [Risk Configuration in Slack DLP for Slack Pro and Slack Business+ Editions](slack/slack_pro_policy/policy_risk.md)
  * [Manage Events for Slack](slack/slack_pro_policy/events.md)
* [Configuring Policies for the Slack Enterprise Edition](slack/enterprise_policy/README.md)
  * [Slack App Selection](slack/enterprise_policy/integration.md)
  * [Configure Scope for Slack Enterprise](slack/enterprise_policy/scope.md)
  * [Select Detection Rules for Slack Enterprise](slack/enterprise_policy/detection_rules.md)
  * [Configure Automated Actions in Slack Enterprise](slack/enterprise_policy/automated_actions.md)
  * [Configure Advanced Settings for Slack Enterprise](slack/enterprise_policy/advanced_settings.md)
  * [Risk Configuration for Slack Enterprise](slack/enterprise_policy/risk_configuration.md)
  * [Manage Events for Slack Enterprise](slack/enterprise_policy/events.md)
* [FAQs](slack/slack-faqs/README.md)
  * [Can I redact sensitive message content in Slack?](slack/slack-faqs/redact_sensitive_data.md)
  * [Nightfall for Slack Pro vs Enterprise](slack/slack-faqs/pro_vs_enterprise/README.md)
    * [Upgrading from Slack Pro to Enterprise](slack/slack-faqs/pro_vs_enterprise/upgrading-pro-to-enterprise.md)
  * [Can we customize the alert messages sent in Slack?](slack/slack-faqs/slack_alert_customization.md)
  * [Can I Disable Detection in Private Channels or DMs?](slack/slack-faqs/detection_disable.md)
  * [What types of channels does Nightfall scan? Does Nightfall scan shared channels?](slack/slack-faqs/types_of_channels_scanned.md)
  * [I am unable to view a sensitive message or file from the Nightfall alert channel.](slack/slack-faqs/alert_message_blocked.md)
  * [Upon Slack installation, why am I seeing a 400 error mentioning a "Restricted Action"?](slack/slack-faqs/slack_400_error.md)
  * [I send a sensitive message, edit it, and then admin applies the Redact action. What is the outcome?](slack/slack-faqs/multiple_actions.md)
  * [How do I re-install Nightfall DLP for Slack Pro Edition?](slack/slack-faqs/reinstall_slack_pro.md)
  * [How do I re-install Nightfall DLP for Slack Enterprise Edition?](slack/slack-faqs/reinstall_slack_enterprise.md)
  * [Our Slack Admin has Quit. Will it impact Nightfall Scan?](slack/slack-faqs/our-slack-admin-has-quit.-will-it-impact-nightfall-scan.md)

## Nightfall for GitHub <a href="#github" id="github"></a>

* [Getting Started](github/getting_started/README.md)
  * [Requirements](github/getting_started/requirements.md)
  * [Install Nightfall for GitHub](github/getting_started/installation.md)
  * [Configure Alerts for GitHub](github/getting_started/integration_alerts.md)
* [Configure Policies for GitHub](github/policies/README.md)
  * [GitHub App Selection](github/policies/integration.md)
  * [Configure Scope for GitHub](github/policies/scope/README.md)
    * [Use Regular Expressions to Exclude GitHub Directories](github/policies/scope/github_regexp.md)
  * [Configure Detection Rules for GitHub](github/policies/detection_rules.md)
  * [Configure Advanced Settings for GitHub](github/policies/advanced_settings.md)
  * [Configure Risk Score for GitHub](github/policies/risk_score.md)
* [Manage GitHub Events](github/events.md)
* [Remediation on Nightfall for Github](github/remediation.md)

## NIGHTFALL FOR GOOGLE DRIVE <a href="#google-drive" id="google-drive"></a>

* [Getting Started](google-drive/getting_started/README.md)
  * [Requirements](google-drive/getting_started/requirements.md)
  * [Install Nightfall for Google Drive](google-drive/getting_started/installation.md)
  * [Enable Google Drive Labels](google-drive/getting_started/labels.md)
  * [Configure Alerts for Google Drive](google-drive/getting_started/integration_alerts.md)
* [Configure Policies for Google Drive](google-drive/policies/README.md)
  * [Google Drive App Selection](google-drive/policies/integration.md)
  * [Configure Scope for Google Drive](google-drive/policies/scope.md)
  * [Configure Detection Rules for Google Drive](google-drive/policies/detection_rules.md)
  * [Configure Advanced Settings for Google Drive](google-drive/policies/advanced_settings.md)
  * [Risk Score for Google Drive](google-drive/policies/configure_risk.md)
  * [Manage Google Drive Events](google-drive/policies/events.md)

## Nightfall for Confluence <a href="#confluence" id="confluence"></a>

* [Getting Started](confluence/getting_started.md)
* [Install Nightfall for Confluence](confluence/installation/README.md)
  * [Configure Alerts for Confluence](confluence/installation/integration_alerts.md)
* [Configuring Policies for Confluence](confluence/policies/README.md)
  * [Confluence App Selection](confluence/policies/integration.md)
  * [Configure Scope for Confluence](confluence/policies/scope.md)
  * [Configure Detection Rules for Confluence](confluence/policies/detection_rules.md)
  * [Configure Advanced Settings for Confluence](confluence/policies/advanced_settings.md)
  * [Configure Risk Score for Confluence](confluence/policies/risk_score.md)
  * [Manage Confluence Events](confluence/policies/events.md)
* [FAQs](confluence/faqs/README.md)
  * [Page Restrictions](confluence/faqs/page-restrictions.md)

## Nightfall for jira <a href="#jira" id="jira"></a>

* [Getting Started](jira/getting_started.md)
* [Install Nightfall for Jira](jira/installation/README.md)
  * [Configuring Alerts for Jira](jira/installation/integration_alerts.md)
* [Configure Policies in Nightfall for Jira](jira/policies/README.md)
  * [Jira App Selection](jira/policies/integration.md)
  * [Configure Scope in Nightfall for JIRA](jira/policies/scope.md)
  * [Select Detection Rules in Nightfall for JIRA](jira/policies/detection_rules.md)
  * [Configuring Advanced Settings in Nightfall for JIRA](jira/policies/advanced_settings.md)
  * [Configure Risk Score for Jira](jira/policies/risk_score.md)
  * [Manage Jira Events](jira/policies/events.md)

## Nightfall for Microsoft 365 <a href="#microsoft-365" id="microsoft-365"></a>

* [Getting Started](microsoft-365/getting_started/README.md)
  * [Microsoft 365 Requirements](microsoft-365/getting_started/requirements.md)
  * [Setting up Directory Sync](microsoft-365/getting_started/directory_sync.md)
  * [Setting up Microsoft Tenant](microsoft-365/getting_started/microsoft_tenant_setup/README.md)
    * [Update App Selection for a Registered Tenant](microsoft-365/getting_started/microsoft_tenant_setup/update_app_selections.md)
* [Nightfall for OneDrive](microsoft-365/onedrive/README.md)
  * [Configure Alerts for OneDrive](microsoft-365/onedrive/integration_alerts.md)
  * [Nightfall Policies for OneDrive](microsoft-365/onedrive/policies/README.md)
    * [OneDrive App Selection](microsoft-365/onedrive/policies/integration.md)
    * [Configure Scope for OneDrive](microsoft-365/onedrive/policies/scope.md)
    * [Configure Detection Rules for OneDrive](microsoft-365/onedrive/policies/detection_rules.md)
    * [Configure Advanced Settings for OneDrive](microsoft-365/onedrive/policies/advanced_settings.md)
    * [Risk Score for OneDrive Policies](microsoft-365/onedrive/policies/risk_score.md)
    * [Manage OneDrive Events](microsoft-365/onedrive/policies/events.md)
* [Nightfall for Microsoft Teams](microsoft-365/microsoft_teams/README.md)
  * [Configure Alerts for Microsoft Teams](microsoft-365/microsoft_teams/integration_alerts.md)
  * [Configure Policies for Microsoft Teams](microsoft-365/microsoft_teams/policies/README.md)
    * [Select Integration in Microsoft Teams](microsoft-365/microsoft_teams/policies/integration.md)
    * [Configure Scope for Microsoft teams](microsoft-365/microsoft_teams/policies/scope/README.md)
      * [Scope for Personal Chats](microsoft-365/microsoft_teams/policies/scope/personal_chats.md)
      * [Scope for MS Teams Channels](microsoft-365/microsoft_teams/policies/scope/channels.md)
    * [Configure Detection Rules in Microsoft Teams DLP](microsoft-365/microsoft_teams/policies/detection_rules.md)
    * [Configure Advanced Settings in Microsoft Teams](microsoft-365/microsoft_teams/policies/advanced_settings.md)
    * [Risk Score in Microsoft Teams Policies](microsoft-365/microsoft_teams/policies/risk_score.md)
    * [Manage Microsoft Teams Events](microsoft-365/microsoft_teams/policies/events.md)

## Nightfall for Microsoft Exchange Online <a href="#microsoft-exchange" id="microsoft-exchange"></a>

* [Getting Started](microsoft-exchange/getting_started/README.md)
  * [Microsoft Exchange Requirements](microsoft-exchange/getting_started/requirements.md)
  * [Setting up Directory Sync](microsoft-exchange/getting_started/directory_sync.md)
  * [Installing Microsoft Exchange](microsoft-exchange/getting_started/installing-microsoft-exchange/README.md)
    * [Create Connectors](microsoft-exchange/getting_started/installing-microsoft-exchange/create-connectors.md)
    * [Create Rules](microsoft-exchange/getting_started/installing-microsoft-exchange/create-rules.md)
    * [Create MX Record](microsoft-exchange/getting_started/installing-microsoft-exchange/create-mx-record.md)
* [Nightfall for Microsoft Exchange](microsoft-exchange/exchange_online/README.md)
  * [Configure Alerts for Exchange](microsoft-exchange/exchange_online/integration_alerts.md)
  * [Configure Policies for Exchange](microsoft-exchange/exchange_online/policies/README.md)
    * [Select Integration in Exchange](microsoft-exchange/exchange_online/policies/integration.md)
    * [Configure Scope for Exchange](microsoft-exchange/exchange_online/policies/scope.md)
    * [Configure Detection Rules in Exchange](microsoft-exchange/exchange_online/policies/detection_rules.md)
    * [Configure Advanced Settings in Exchange](microsoft-exchange/exchange_online/policies/advanced_settings.md)
    * [Risk Score in Exchange](microsoft-exchange/exchange_online/policies/risk_score.md)
    * [Manage Exchange Events](microsoft-exchange/exchange_online/policies/events.md)

## Nightfall for Microsoft Sharepoint <a href="#microsoft-exchange" id="microsoft-exchange"></a>

* [Getting Started](microsoft-exchange-1/getting_started/README.md)
  * [Microsoft SharePoint Requirements](microsoft-exchange-1/getting_started/requirements.md)
  * [Setting up Directory Sync](microsoft-exchange-1/getting_started/directory_sync.md)
  * [Installing Microsoft SharePoint](microsoft-exchange-1/getting_started/installing-microsoft-sharepoint.md)
* [Nightfall for Microsoft SharePoint](microsoft-exchange-1/exchange_online/README.md)
  * [Configure Alerts for SharePoint](microsoft-exchange-1/exchange_online/integration_alerts.md)
  * [Configure Policies for SharePoint](microsoft-exchange-1/exchange_online/policies/README.md)
    * [Select Integration in SharePoint](microsoft-exchange-1/exchange_online/policies/integration.md)
    * [Configure Scope for SharePoint](microsoft-exchange-1/exchange_online/policies/scope.md)
    * [Configure Detection Rules in SharePoint](microsoft-exchange-1/exchange_online/policies/detection_rules.md)
    * [Configure Advanced Settings in SharePoint](microsoft-exchange-1/exchange_online/policies/advanced_settings.md)
    * [Risk Score in SharePoint](microsoft-exchange-1/exchange_online/policies/risk_score.md)
    * [Manage SharePoint Events](microsoft-exchange-1/exchange_online/policies/events.md)

## Nightfall for Gmail  <a href="#gmail" id="gmail"></a>

* [Overview](gmail/overview.md)
* [Install Nightfall DLP for Gmail](gmail/installation/README.md)
  * [Configure Content Compliance Rules](gmail/installation/content_compliance_rules/README.md)
    * [Create Content Compliance Rule - Monitoring](gmail/installation/content_compliance_rules/monitroring.md)
    * [Create Content Compliance Rule - Monitoring](gmail/installation/content_compliance_rules/monitroring-1.md)
    * [Configure Content Compliance Rule - Quarantine](gmail/installation/content_compliance_rules/quarantine.md)
    * [Configure Routing Rules - SMTP Relay Settings](gmail/installation/content_compliance_rules/smtp_relay_settings.md)
* [Configure Alerts for Gmail](gmail/integration_alerts.md)
* [Nightfall Policies for Gmail](gmail/policies/README.md)
  * [Gmail App Selection](gmail/policies/integration.md)
  * [Configure Scope for Gmail](gmail/policies/scope.md)
  * [Configure Detection Rules for Gmail](gmail/policies/detection_rules.md)
  * [Configure Advanced Settings for Gmail](gmail/policies/advanced_settings.md)
  * [Configure Risk Score for Gmail](gmail/policies/risk_score.md)
  * [Manage Gmail Events](gmail/policies/events.md)
* [Remediation on Nightfall for Gmail](gmail/remediation.md)

## Nightfall For Salesforce <a href="#salesforce" id="salesforce"></a>

* [Overview](salesforce/overview.md)
* [Getting Started](salesforce/getting-started/README.md)
  * [Install Nightfall DLP for Salesforce](salesforce/getting-started/installation.md)
  * [Upgrade Nightfall DLP for Salesforce](salesforce/getting-started/upgrade.md)
  * [Configure Alerts for Salesforce](salesforce/getting-started/integration_alerts.md)
* [Nightfall Policies for Salesforce](salesforce/policies/README.md)
  * [Salesforce App Selection](salesforce/policies/integration.md)
  * [Configure Scope for Salesforce](salesforce/policies/scope.md)
  * [Configure Detection Rules for Salesforce](salesforce/policies/detection_rules.md)
  * [Configure Advanced Settings for Salesforce](salesforce/policies/advanced_settings.md)
  * [Risk Score for Salesforce](salesforce/policies/risk_score.md)
  * [Manage Salesforce Events](salesforce/policies/events.md)
* [FAQs](salesforce/faqs.md)

## Nightfall for Zendesk <a href="#zendesk" id="zendesk"></a>

* [Getting Started](zendesk/getting_started/README.md)
  * [Requirements](zendesk/getting_started/requirements.md)
  * [Install Nightfall DLP for Zendesk](zendesk/getting_started/installation.md)
  * [Configure Alerts for Zendesk](zendesk/getting_started/integration_alerts.md)
* [Configure Policies for Zendesk](zendesk/policies/README.md)
  * [Zendesk App Selection](zendesk/policies/integration.md)
  * [Configure Scope for Zendesk](zendesk/policies/scope.md)
  * [Configure Detection Rules for Zendesk DLP](zendesk/policies/detection_rules.md)
  * [Configure Advanced Settings in Zendesk](zendesk/policies/advanced_settings.md)
  * [Risk Score for Zendesk](zendesk/policies/risk_score.md)
  * [Manage Zendesk Events](zendesk/policies/events.md)

## Nightfall for Notion <a href="#notion" id="notion"></a>

* [Getting Started](notion/getting_started/README.md)
  * [Requirements](notion/getting_started/requirements.md)
  * [Steps](notion/getting_started/steps.md)
* [Install Nightfall for Notion](notion/installation/README.md)
  * [Verification of Notion Installation](notion/installation/verification.md)
* [Configure Alerts for Notion](notion/integration_alerts.md)
* [Configure Policies for Notion](notion/policies/README.md)
  * [Notion App Selection](notion/policies/integration.md)
  * [Configure Detection Rules for Notion](notion/policies/detection_rules.md)
  * [Configure Advanced Settings for Notion](notion/policies/advanced_settings.md)
  * [Risk Score for Notion](notion/policies/risk_score.md)
  * [Manage Notion Events](notion/policies/events.md)

## NIGHTFALL FOR Generative AI Applications <a href="#gen-ai" id="gen-ai"></a>

* [Overview](gen-ai/overview.md)
* [Install Nightfall for GenAI apps](gen-ai/installation/README.md)
  * [Install Nightfall DLP on Individual Devices](gen-ai/installation/individual_devices.md)
  * [Install Nightfall DLP Across Organization](gen-ai/installation/mdm.md)
  * [Install Nightfall DLP with Microsoft Intune](gen-ai/installation/install-nightfall-dlp-with-microsoft-intune.md)
* [Configure Alerts for GenAI apps](gen-ai/integration_alerts.md)
* [Creating GenAI Policies from Nightfall Console](gen-ai/policies/README.md)
  * [AI Apps Selection](gen-ai/policies/integration.md)
  * [Configure Detection Rules for AI Apps](gen-ai/policies/detection_rules.md)
  * [Configure Advanced Settings for AI Apps](gen-ai/policies/advanced_settings.md)
  * [Risk Score for AI Apps](gen-ai/policies/risk_score.md)
* [Nightfall Browser Plugin Deployment Guide](gen-ai/deployment_guide.md)
* [GenAI Safe Usage and Data Protection Policy](gen-ai/safety_guide.md)

## Developer Section

* [Nightfall Firewall for AI](https://help.nightfall.ai/nightfall-developer-platform/)
* [Nightfall Playground](https://playground.nightfall.ai/)

## Settings <a href="#nightfall_settings" id="nightfall_settings"></a>

* [Users and Roles](nightfall_settings/users_roles/README.md)
  * [Authentication Options](nightfall_settings/users_roles/authentication_options.md)
* [Role Based Access Control (RBAC)](nightfall_settings/role_based_access_control/README.md)
  * [Security Analyst Role](nightfall_settings/role_based_access_control/security_analyst.md)
  * [Policy Manager Role](nightfall_settings/role_based_access_control/policy_manager.md)
  * [Security Events Manager Role](nightfall_settings/role_based_access_control/security_events_manager.md)
  * [Security Operations Manager Role](nightfall_settings/role_based_access_control/security_operations_manager.md)
  * [System Administrator Role](nightfall_settings/role_based_access_control/system_administrator.md)
* [Directory Sync](nightfall_settings/directory_sync/README.md)
  * [Add Microsoft Entra ID to Nightfall](nightfall_settings/directory_sync/microsoft_entra_id.md)
  * [Google Workspace Directory Service](nightfall_settings/directory_sync/google_workspace.md)
  * [Add Okta to Nightfall](nightfall_settings/directory_sync/okta.md)
* [Custom Branding](nightfall_settings/custom-branding.md)
* [Customer Referral Program](nightfall_settings/customer-referral-program.md)

***

* [Frequently Asked Questions (FAQs)](faqs/README.md)
  * [How long does it take to deploy Nightfall?](faqs/nightfall_deployment_time.md)
  * [How do I deploy Nightfall?](faqs/deploy_nightfall.md)
  * [What are some unique points about Nightfall that I should know?](faqs/differentiators.md)
  * [Which languages does Nightfall support?](faqs/supported_languages.md)
  * [How does Nightfall yield time savings for my team?](faqs/reduced_tco.md)
  * [Nightfall vs Legacy DLP: What's the difference?](faqs/nightfall_vs_legacy_dlp.md)
  * [How does Nightfall make my organization more secure?](faqs/eliminate_data_exposure.md)
  * [Nightfall vs CASB: What's the difference?](faqs/nightfall_vs_casb.md)
  * [Nightfall vs E-Discovery: What's the difference?](faqs/nightfall-vs-e-discovery.md)
  * [How does Nightfall classify data?](faqs/data_classification.md)
  * [What types of data does Nightfall classify?](faqs/nightfall_data_types_classification.md)
  * [Does Nightfall scan unstructured data?](faqs/unstructured_data_scan.md)
  * [Does Nightfall require data to be already tagged?](faqs/data_tagging.md)
  * [How do I learn more about and test out Nightfall?](faqs/contact_sales.md)
  * [Using Service Accounts with Nightfall](faqs/service_accounts.md)
  * [Which permissions are required for each integration?](faqs/permissions.md)
  * [Where can I find active user counts for each SaaS application protected by Nightfall?](faqs/active_users.md)
  * [In the Atlassian Marketplace, why does it show that the Nightfall app is not approved in security?](faqs/atlassian_marketplace.md)
  * [How can I estimate the data volume that Nightfall needs to scan?](faqs/estimate_data_to_be_scanned.md)
  * [How can I check the Platform Status of Nightfall](faqs/platform_status.md)
* [Login to Nightfall](https://app.nightfall.ai)
* [Contact Nightfall](contact-us.md)
* [Nightfall Page Redirects](nightfall-page-redirects.md)
