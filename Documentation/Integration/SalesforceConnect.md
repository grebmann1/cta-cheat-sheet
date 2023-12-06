[Table of Contents](../Documentation.md)

# Integration - Salesforce Connect

## When to Use Salesforce Connect?

1. Real-time access of data existing in another system without importing the data.
2. Data shouldn't be stored in Salesforce but synchronized in real-time.
3. Creation or modification of external data from Salesforce.

### Actions Supported

1. Reports
2. Record Feed (No Field History Tracking)
3. Flow & Process Builder (No Approval process)
4. Quick Actions (No Task Creation)

## External Objects

External Object (__x) represents virtualized objects using the OData protocol and can be linked with:

- External Lookup Relationship
    - Standard/Custom ⟶ External Object
    - External Object ⟶ External Object
- Indirect Lookup Relationship (External object as the child)
    - External Object ⟶ Standard/Custom Object

## High Data Volume Considerations

Some features are no longer available due to high data volume:

- Access via Lightning Experience
- Access via Salesforce Mobile App
- Record Feeds
- Writable external objects
- Salesforce console
- Reports and Dashboards
- Salesforce ID assignment

## Sharing

Controlling the sharing of External Objects is currently not possible. There are a few ways to provide visibility control:

1. Use LWC with Apex Controller to provide access to the user (Visibility controlled in Apex).
2. Sharing/visibility controlled on the server side (User context parameter provided when configuring the Named Credential).
3. Restriction Rules (Max 5 / Objects) ([More details](https://help.salesforce.com/s/articleView?id=release-notes.rn_forcecom_sharing_restriction_rules_external_objects.htm&release=238&type=5)).

### Salesforce Connect Adapters

Adapters available for Salesforce Connect:

| Adapter | Description | When to Use |
|---------|-------------|--------------|
| Cross-org | Uses the Lightning Platform REST API to access data in other Salesforce orgs. | Connect data between your Salesforce orgs. |
| OData (2.0, 4.0 & 4.01) | Uses Open Data Protocol to access data outside Salesforce. | Integrate external data sources into your org supporting the ODATA protocol. |
| Custom adapter via Apex | Develop your own adapter with the Apex Connector Framework. | Retrieve data via callouts from a REST API. |
| Salesforce Connect Adapter for Amazon DynamoDB | Connects Amazon DynamoDB data sources to Salesforce through external objects. | Integrate AWS data natively with Salesforce. |
| Salesforce Connect Adapter for Amazon Athena | Utilizes Amazon Athena’s capability to run queries against data directly in Amazon S3. | Integrate AWS data natively with Salesforce and run interactive on-demand queries. |
| Salesforce Connect Adapter for GraphQL | Uses GraphQL APIs to integrate applications. | Access data from external sources exposing capabilities via GraphQL. |

### Salesforce Connect Adapters Included per Add-On License

| Adapter | Number of Connections | Comments |
|---------|-----------------------|----------|
| Cross-org | 5 |
| Others | 1 |

### Limitations & Allocations for Salesforce Connect

| Description | Unlimited, Enterprise & Performance | Comment |
|-------------|------------------------------------|---------|
| Maximum external objects per org. | 200 | **[Hard Limit]** |
| Maximum new rows retrieved by SOSL and Salesforce searches per hour. | 100k | High-data-volume external data sources excluded. |
| Maximum new rows retrieved or created per hour. | 100k | High-data-volume external data sources, rows retrieved as search results only, and other already retrieved rows excluded. |
| Maximum page size for server-driven paging. | 2k rows |

### Callout Limits for Salesforce Connect Adapters

| Description | Unlimited, Enterprise & Performance | Comment |
|-------------|------------------------------------|---------|
| Cross-org adapter | No callout limits | API Usage limit applies on the provider org. |
| OData 2.0 and 4.0 | 20k/hour | **Add-on** available to increase limits. |
| OData 4.01 | No callout limits |
| Custom Adapter | Callout and Apex Execution limits apply | Built-in Apex using the Apex Connector Framework. |
| Amazon DynamoDB, Amazon Athena | No callout limits |
| GraphQL | No callout limits |

## External Change Data Capture

It's possible to enable `External Change Data Capture` to track changes outside of Salesforce (5-30 minutes delay) and interact with an Apex or Flow event triggered.

## Documentation

1. [Access External Data With Salesforce Connect](https://help.salesforce.com/s/articleView?id=sf.salesforce_connect.htm&type=5)
