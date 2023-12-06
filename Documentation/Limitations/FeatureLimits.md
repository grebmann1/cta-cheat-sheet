[Table of Contents](../Documentation.md)

# Limitations - Feature Limits

## Sales Cloud
### Web to Lead 
With Web-to-Lead, you can capture up to `500 leads in a 24-hour period`. This operates similarly to the Web-to-Case queue.

## Service Cloud
### Web to Case

With Web-to-Case, you can capture up to `5,000 cases in a 24-hour period`. If the number exceeds this limit, the pending requests are added to a queue that can contain a maximum of 50,000 requests (Web-to-Case and Web-to-Lead combined).

## Platform
### General Email Limits
Salesforce orgs can send single emails to a `maximum of 5,000 external email addresses per day`.
- Single emails sent using the email author or composer in Salesforce don't count towards this limit.
- There's no limit on sending single emails to contacts, leads, person accounts, and users in your organization directly from the Account, Contact, Lead, Opportunity, Case, Campaign, or custom object pages.

Visualforce email templates can't be used for "Mass Emailing".
