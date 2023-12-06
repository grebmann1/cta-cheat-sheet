[Table of Contents](../Documentation.md)

# Integration - General

## List of Most Common Integration Patterns

| Pattern                      | Description                                                    |
|------------------------------|----------------------------------------------------------------|
| Request & Reply               | Call and wait for the process to complete                      |
| Fire & Forget                 | Call and doesn't wait for the process to complete             |
| Batch Data Synchronization    | Update data with Batch (Bulk API)                              |
| Remote Call-In                | Target system receives a remote system call to CRUD data        |
| UI Update Based on Data Change| Listen to push topics (Stream) and display information in UI    |
| Data Virtualization           | Use Salesforce Connect to create an External Object (OData)     |

## Technologies

Different technologies can be used to connect systems together such as:
- REST API
- SOAP API
- Streaming API (Events)
    - [Change Data Capture](ChangeDataCapture.md)
    - [Platform Event](PlatformEvent.md)
    - Kafka (Apache)
- OData (Data Virtualization)
    - [Salesforce Connect](SalesforceConnect.md)
