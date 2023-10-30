# Mobile Solution
In the modern world, more & more company are using mobile app to interact with their clients and/or customers.

Salesforce propose 3 solutions:
- Salesforce Mobile App
- Mobile Publisher
- Mobile SDK (in combo with Native or Hybrid solution)

# Salesforce Mobile App
The Salesforce mobile app is Salesforce on the go!\
This enterprise mobile experience gives you access to the same information you see in the office, but organized for getting work done between customer meetings, while waiting for a flight, even when you’re in line for coffee.

Salesforce Mobile App is supporting `Offline Capabilities`.

# Mobile Publisher

Use Mobile Publisher to create a customized and branded Experience Cloud mobile app. When your users can identify the app with your brand, they’re more likely to use it, which increases adoption.

### Licenses
A `Salesforce Mobile Publisher` license is required to be able to publish the app.

### Limitation
Offline capabilities are limited. In case there is a need for offline capabilities, it's better to consider an hybrid solution using the salesforce mobile SDK.

# Mobile SDK (Recommended)

With mobile SDK, you can interact with Salesforce data directly from your mobile and take advantages of key functionnalities such as : 
- `Offline Capabitilies`
- Push notifications

Mobile SDK can be used with LWC and/or REACT to build an Hybrid app on top of Experience Cloud (To manage the users)

As an example, a customer app would include:
- Experience Cloud (User access & management via API )
- Mobile App with Salesforce Mobile SDK (Hybrid with LWC support)