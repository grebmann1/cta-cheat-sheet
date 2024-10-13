[Table of Contents](../Documentation.md)

# Event Monitoring

## Basic OOTB solution
Salesforce is only providing basing monitoring capabilities OTB such as :
- User Login Monitoring

## Real Time Event Monitoring (Add-on)

An Add-on [Event Monitoring](../Product%20&%20Clouds/addOn_ShieldEventMonitoring.md) can be purchased to extend the functionality such as :
- **Security Enhancement**: Monitoring login attempts, API usage, and data access to detect and prevent security threats.
- **Compliance Assurance**: Ensuring adherence to regulatory requirements by tracking user actions and access to sensitive data.
- **Insightful Analytics**: Gaining insights into system performance, user adoption rates, and overall platform usage patterns.

### Log Storage Overview
Real-Time Event Monitoring allows for the storage of large volumes of event data in both *big objects* and *standard objects*. These objects can store data for up to 6 months, with exceptions like IdentityVerificationEvent and LoginEvent, which can store data for up to 10 years.

Key points about storage:
- **Big Objects**: Used for high-volume data storage (e.g., API events, login events). Limited to querying by EventDate or EventIdentifier.
- **Standard Objects**: Used for events like Threat Detection and session hijacking. Full SOQL queries can be used on all fields.
- **Async SOQL**: Best for handling large data sets, especially for big objects, as it allows for background query processing.

**Storage Duration**: `In most cases, data is stored for up to 6 months`, except in Developer Edition orgs, where it's only stored for one day.

