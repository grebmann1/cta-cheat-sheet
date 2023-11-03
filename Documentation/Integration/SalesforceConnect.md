[Table of contents](../Documentation.md) / [Integration](Integration.md)
# Integration - Salesforce Connect 

### When to use Salesforce Connect ?

 1. Real time access of data existing in another system without importing the data
 2. Data shouldn't be stored in Salesforce but Real time synchronization.
 3. External Data need to be created or modified from Salesforce

### Action Supported
 1. Reports
 2. Record Feed (No Field History Tracking)
 3. Flow & Process Builder (No Approval process)
 4. Quick Actions (No Task Creation)

### External Objects
External Object (__x) are representing the objects that are virtualized using the OData protocol. These objects can be linked with : 
- External Lookup Relationship
    - Standard/Custom &rarr;  External Object
    - External Object &rarr;  External Object
- Indirect Lookup Relationship (The external object is the child)
    - External Object &rarr; Standard/Custom Object

### High Data Volume Considerations
If your org hits rate limits when accessing external objects, consider selecting the High Data Volume option on the associated external data sources. Doing so bypasses most rate limits, but some special behaviors and limitations apply.

These features aren't available anymore:
 - Access via Ligning Experience
 - Access via the Salesforce mobile app
 - Records Feeds
 - Writable external objects
 - Salesforce console
 - Report and Dashboard
 - Salesforce Id assignment

### Sharing
It's currently not possible to control the sharing of External objects. There is currently only a few way to provide some kind of visibility control:
1. Use LWC with Apex Controller to provie access to the user (Visibility controlled in Apex)
2. `Sharing/visibility controlled on the server side` (User context parameter can be provided when configuring the Named Credential)

#### Salesforce Connect Adapters
These adapter are available for Salesforce Connect

| Adapter | Description | When to use |
|--|--|--|
|Cross-org| Uses the Lightning Platform REST API to access data that’s stored in other Salesforce orgs.|To connect data between your Salesforce orgs. For example, provide your service representatives a unified view of customer transactions by integrating data from different Salesforce orgs.
|Odata (2.0,4.0 & 4.01) | Uses Open Data Protocol to access data that’s stored outside Salesforce. The external data must be exposed via OData producers. |To integrate external data sources into your org that support the ODATA protocol and publish an OData provider. For example, give your account executives a unified data view by pulling data from legacy systems such as SAP, Microsoft, and Oracle in real time.
|Custom adapter created via Apex| Uses the Apex Connector Framework to develop your own custom adapter when the other available adapters aren’t suitable for your needs. A custom adapter can obtain data from anywhere. For example, some data can be retrieved from anywhere in the Internet via callouts, while other data can be manipulated or even generated programmatically.| To develop your own adapter with the Apex Connector Framework when the other available adapters aren’t suitable for your needs. For example, when you want to retrieve data via callouts from a REST API.
|Salesforce Connect Adapter for Amazon DynamoDB | Connects Amazon DynamoDB data sources to Salesforce through external objects. The data stored in Amazon DynamoDB can use the flexible data storage option of DynamoDB and Salesforce Platform capabilities.| To integrate AWS data natively with Salesforce business applications.
|Salesforce Connect Adapter for Amazon Athena| Takes advantage of Amazon Athena’s capability to run queries against data directly in Amazon Simple Storage Service (S3) without having to manage RDBMS infrastructure or ETL tools.|To integrate AWS data natively with Salesforce and run interactive on demand queries.
|Salesforce Connect Adapter for GraphQL |Uses GraphQL APIs to provide a modern way to integrate applications.|To access and integrate data from external sources that expose their capabilities via GraphQL.

#### Salesforce Connect Adapters Included per Add-On License
| Adapter | Number of Connections | Comments
|--|--|--|
|Cross-org| 5
|Others| 1

#### Limitations & Allocations for Salesforce Connect 
| Description | Unlimited, Enterprise & Performance | Comment |
|--|--|--|
| Maximum external objects per org.| `200` |  **[Hard Limit]**
| Maximum new rows retrieved by SOSL and Salesforce searches per hour.| `100k` | This limit doesn’t apply to high-data-volume external data sources.
| Maximum new rows retrieved or created per hour.| `100k` | This limit doesn’t apply to: High-data-volume external data sources,Rows that are retrieved only as search results and aren’t opened or edited, Other rows that have already been retrieved
|Maximum page size for server-driven paging. | 2k rows 

#### Callout Limits for Salesforce Connect Adapters
| Description | Unlimited, Enterprise & Performance | Comment |
|--|--|--|
|Cross-org adapter | No callout limits |API Usage limit apply on the provider org.
| Odata 2.0 and 4.0| `20k/hour`| **Add on** available to increase the limits.
| Odata 4.01 | `No callout limits`
| Custom Adapter | Callout and Apex Execution limits apply | Adapter built in apex using the Apex Connector Framework.
| Amazon DynamoDN, Amazon Athena| No callout limits
| GraphQL | No callout limits


### Documentation

1. [Access External Data With Salesforce Connect](https://help.salesforce.com/s/articleView?id=sf.salesforce_connect.htm&type=5)