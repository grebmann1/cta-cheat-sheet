[Table of Contents](../Documentation.md)

# Event Monitoring

Event Monitoring within Salesforce is a feature designed to track and analyze user activities and interactions within the Salesforce platform. It captures event-level data to provide comprehensive insights into user behavior, system usage, security, and compliance.

## Licenses
Salesforce Event Monitoring is provided via an `Platform License` (No User license).

## Purpose
The primary objectives of Event Monitoring in Salesforce include:

- **Security Enhancement**: Monitoring login attempts, API usage, and data access to detect and prevent security threats.
- **Compliance Assurance**: Ensuring adherence to regulatory requirements by tracking user actions and access to sensitive data.
- **Insightful Analytics**: Gaining insights into system performance, user adoption rates, and overall platform usage patterns.


## Event Log Files

Data from events is stored in log files, accessible through Salesforce's Event Monitoring API or third-party log analysis tools. Different log types exist for various activities such as logins, API usage, and report access.

#### Event Monitoring Apps:

Consider leveraging third-party applications or integrations to visualize and analyze event data for enhanced insights.

## Enhanced Transaction Security

Enhanced Transaction Security is a framework that intercepts real-time events and applies appropriate actions to monitor and control user activity.\
Each transaction security policy has conditions that evaluate events and the real-time actions that are triggered after those conditions are met.

### Policies
Policies can be build with the `Condition Builder` or via `Apex`.\
You can create transaction security policies on these `Real-Time Event Monitoring events`.

| Event Type| Description|
|-----------|------------|
| ApiEvent Policies| Monitors API transactions, such as SOQL queries and data exports.|
| ApiAnomalyEventStore Policies| Monitors anomalies in how users make API calls.|
| BulkApiResultEventStore Policies| Detects when a user downloads the results of a Bulk API request.|
| CredentialStuffingEventStore Policies| Monitors successful logins during identified credential stuffing attacks, which involves automated login requests using stolen credentials on a large scale.|
| FileEvent Policies| Detects file-related events, such as when a user downloads a file containing sensitive information.|
| ListViewEvent Policies| Monitors data viewing or downloading from list views using Salesforce Classic, Lightning Experience, or the API.|
| LoginEvent Policies| Tracks login activity and enforces login requirements.|
| PermissionSetEventStore Policies| Monitors critical permission assignment in permission sets.|
| ReportEvent Policies| Monitors data viewing or downloading from reports.|
| ReportAnomalyEventStore Policies| Monitors anomalies in how users run or export reports.|
| SessionHijackingEventStore Policies | Monitors instances when unauthorized users gain control of a Salesforce user's session using a stolen session identifier.|




