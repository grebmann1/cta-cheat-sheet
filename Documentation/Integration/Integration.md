[Home](../../README.md)
# Integration - General 

## List of most common integration patterns

| Pattern| Description|
|-----------------------|---------------------------------------------------------|
| Request & Reply| Call and wait for the process to complete|
| Fire & Forget| Call and doesn't wait for the process to complete|
| Batch Data Synchronization | Update data with Batch (Bulk API)|
| Remote Call-In | Target system receives a remote system call to create, retrieve, update, or delete data by a remote system (e.g., call the Salesforce Enterprise API) |
| UI Update Based on Data Change | Listen to push topics (Stream) and display the information in the UI |
| Data Virtualization| Use Salesforce Connect to create an External Object (OData) |

## Technologies
Differents technologies can be used to connect systems togethers such as :
- REST API
- SOAP API
- Streaming API (Events)
    - [ChangeDataCapture](ChangeDataCapture.md)
    - [PlatformEvent](PlatformEvent.md)
    - Kafka (Apache)
- OData (Data Virtualization)
    - [Salesforce Connect](SalesforceConnect.md)