[Table of Contents](../Documentation.md)

# Mobile Solutions

In today's modern world, an increasing number of companies are utilizing mobile apps to engage with their clients and customers effectively.

Salesforce offers three solutions:
- Salesforce Mobile App
- Mobile Publisher
- Mobile SDK (in combination with Native or Hybrid solutions)

## Salesforce Mobile App

The Salesforce mobile app is your Salesforce platform on the go! This enterprise mobile experience provides access to the same information available in the office, conveniently organized for productivity during customer meetings, while traveling, or even while waiting in line for coffee.

The Salesforce Mobile App supports `Offline Capabilities`.

## Mobile Publisher

Utilize Mobile Publisher to create a customized and branded Experience Cloud mobile app. When your users can associate the app with your brand, they are more likely to use it, leading to increased adoption.

### Licenses

A `Salesforce Mobile Publisher` license is required to publish the app.

### Limitations

Offline capabilities are restricted. For comprehensive offline capabilities, it's advisable to consider a hybrid solution using the Salesforce Mobile SDK as offline capabilities with LWC (Lightning Web Components) are limited and/or in beta.

## Mobile SDK (Recommended)

With the Mobile SDK, you can directly interact with Salesforce data from your mobile device and leverage key functionalities such as:
- `Offline Capabilities`
- Push notifications

The Mobile SDK can be used with LWC and/or REACT to build a Hybrid app on top of Experience Cloud (for user management).

For instance, a customer app might include:
- Experience Cloud (User access & management via API)
- Mobile App with Salesforce Mobile SDK (Hybrid with LWC support)

### Push Notifications

Push notifications can be sent directly from Salesforce via Flow and/or Apex.

Additionally, Marketing Cloud can be used to engage with customers by sending push notifications.
