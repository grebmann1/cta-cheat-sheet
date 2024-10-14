[Table of Contents](../Documentation.md)

# Limitations - Feature Limits

## Sales Cloud
### Web to Lead 
With Web-to-Lead, you can capture up to `500 leads in a 24-hour period`. This operates similarly to the Web-to-Case queue.

## Service Cloud
### Web to Case

With Web-to-Case, you can capture up to `5,000 cases in a 24-hour period`. If the number exceeds this limit, the pending requests are added to a queue that can contain a maximum of 50,000 requests (Web-to-Case and Web-to-Lead combined).

## Platform

### Custom Notification
#### Overview
- Up to **500 custom notification types** per organization.
- A maximum of **10,000 users** as recipients for each notification after expanding groups, queues, or teams. 
- Up to **10,000 notification actions** can be executed per hour. Any unsent notifications after the limit are lost and resume in the next hour.
#### Viewing Notifications
- **Desktop**: 
  - Users can view notifications from the last **30 days**, with 50 notifications displayed at a time in the tray. Maximum tray size: **10,000 notifications**. Exceeding 7,500 triggers a purge to 5,000 notifications.
  
- **Salesforce Mobile App**: 
  - Users can view up to **20 notifications** at a time, with older notifications accessible via swiping. Notifications older than 30 days are deleted.
  
- **Purge Mechanism**: If the number of notifications exceeds 10,000, the user won’t receive new notifications. A purge job runs daily to maintain 5,000 notifications.

#### Handling Delivery Channels
- **Pausing Delivery**: Disabling a delivery channel (mobile, desktop) halts visibility, but notifications are still created. When re-enabled, stored notifications become visible.
  
- **Mobile Notifications**: 
  - **In-app notifications** require the **Enable in-app notifications setting**. 
  - Push notifications for the Salesforce mobile app require the **Enable push notifications setting**.

---
### General Email Limits
Salesforce orgs can send single emails to a `maximum of 5,000 external email addresses per day`.
- Single emails sent using the email author or composer in Salesforce don't count towards this limit.
- There's no limit on sending single emails to contacts, leads, person accounts, and users in your organization directly from the Account, Contact, Lead, Opportunity, Case, Campaign, or custom object pages.

Visualforce email templates can't be used for "Mass Emailing".

