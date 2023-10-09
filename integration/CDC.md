
# Integration - CDC 

### When to use CDC ?

 1. Real Time Integration
 2. Update external system when change occurred

### Custom Channels
Custom Channels are used to groups events together and to filter events to provide more granular control.
[Custom Channels  are only configurable with **Metadata API**]

### Enriched Fields
Enriched fields are used to include "Extra Field" in the events that are published. 
For CDC, enriched fields are available for "Update" and "Delete". There is up to 10 enriched fields that can be included by channel members. (For a custom channel including Account and Contact, this would mean 2x 10 enriched fields).
[Enriched fields are only configurable with **Metadata API**]

### Filter Event
Events can be filtered using SOQL queries to provide more granular control over the events that are published to the subscribers. (Good to reduce the amount of event published)

### Security
If Salesforce record fields are encrypted with **Shield Platform Encryption**, changes in encrypted field values generate change events. To ensure the events are encrypted (not in clear text), an **event bus tenant secret** need to be created and encryption enabled.

Before delivering a platform event message to a subscribed client, the event payload is decrypted using the encryption key. The platform event message is sent over a secure channel using HTTPS and TLS, which ensures that the data is protected and encrypted while in transit.

(Classic Encryption isn't supported, Shield Platform Encryption need to be enabled)


### Data Life
Events are stored in the event bus for **three days (72h)**. Each event contain a "ReplayId" field that can be use to retrieve the event.

#### Limitations & Allocations
| Description | Unlimited  | Enterprise | Professional | Essential |
|--|--|--|--|--|
|Maximum number of concurrent CometD clients (subscribers) across all channels and for all event types. **[Hard Limit]**|  2000| 1000 |  |  |
|Maximum number of entities, including standard and custom objects, that you can select for Change Data Capture on the default standard channel or a custom channel. **[Add On]** |  5| 5 |  |  |
|Maximum number of custom channels. *This allocation is separate from the one for custom platform event channels.* **[Add On]** |  100| 100|  |  |
|Maximum number of entities, including standard and custom objects, that you can select for Change Data Capture on the default standard channel or a custom channel. If the same entity is selected in multiple channels, it’s counted once toward the allocation. **[Add On]** |  5| 5 |  |  |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours, shared by all clients. (Applies to CometD and Pub/Sub API clients, empApi Lightning components, and event relays only.) **[Add On]** |  50k| 25k |  |  |


#### Change Data Capture add-on license
This add-on can be purchased multiple times. The add-on is increasing the delivery by :
 
 - 100k Daily (500k Technical limit)
 - 3M Monthly
 
| Description | Unlimited  | Enterprise | Professional | Essential |
|--|--|--|--|--|
|Maximum number of entities, including standard and custom objects, that you can select for Change Data Capture on the default standard channel or a custom channel.|  No Limit| No Limit |  |  |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours, shared by all clients. (Applies to CometD and Pub/Sub API clients, empApi Lightning components, and event relays only.)|  Last 24 hours: 150k (50k + 100k) (5x - 550k Hard Limit). Monthly entitlement: 4.5M (1.5M + 3M)| Last 24 hours: 125K (25k  + 100k) (5x - 525k Hard Limit). Monthly entitlement: 3.75M (0.75M + 3M) |  |  |