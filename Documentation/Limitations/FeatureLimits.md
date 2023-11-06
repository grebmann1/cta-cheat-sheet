[Table of contents](../Documentation.md)
# Limitations - Feature Limits


## Sales Clouds
### Web to lead 
With web to lead, you can capture up to `500 leads in a 24h period`. (Queue similar to web to case)

## Service Cloud
### Web to case

With web to case, you can capture up to `5k cases in a 24h period`. If it's above, the pending requests are added to a queue that can contain a maximum of 50k requests (web to case & web to lead combined)

## Platform
### General Email Limits
Salesforce orgs can send single emails to a `maximum of 5k external email addresses per day`.\
- Single emails sent using the email author or composer in Salesforce don't count towards this limit.
- There’s no limit on sending single emails to contacts, leads, person accounts, and users in your organization directly from the Account, Contact, Lead, Opportunity, Case, Campaign, or custom object pages.

Visualforce email template can't be used for "Mass Emailing".
