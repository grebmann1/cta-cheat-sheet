# Integration - Platform Event 

### When to use Platform Event ?

 1. Real Time Integration
 2. Update external/internal system with specific information/event
 3. Execute Async flow/apex with internal subscriber
 4. Monitor execution and/or issues

### How to publish Platform Event ?

 1. Flows
 2. Processes
 3. Apex
 4. Salesforce APIs (REST, SOAP, Pub/Sub)

### Data Life
Events are stored in the event bus for **3 days (72h)** for high volume event ~~and **1 day (24h)** for standard event~~. Each event contain a "ReplayId" field that can be use to retrieve the event.
Standard event are now deprecated (Only available for API < 44.0)

### Security
Before delivering a platform event message to a subscribed client, the event payload is decrypted using the encryption key. The platform event message is sent over a secure channel using HTTPS and TLS, which ensures that the data is protected and encrypted while in transit.

(Classic Encryption isn't supported, Shield Platform Encryption need to be enabled)

#### Delivery VS Publishing
Non-API clients, including Apex triggers, Process Builder processes, and flows, don’t count against the event **delivery limit** but toward the **Publishing limit**.

#### Limitations & Allocations
| Description | Unlimited  | Enterprise | Professional (with API Add-on) | Essential |
|--|--|--|--|--|
|Maximum number of concurrent CometD clients (subscribers) across all channels and for all event types. **[Hard Limit]**|  2000| 1000 | 20 |  |
|Maximum number of platform event definitions that can be created in an org |  100| 50 | 20 |  |
|Maximum number of custom channels that can be created. This allocation is separate from the one for custom change data capture channels.|  100| 100| 100 |  |
|Maximum number of distinct platform events that can be added to a channel as part of channel members.If the same platform event is added to multiple channels, it’s counted once toward the allocation.|  50| 50 | 5 |  |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours, shared by all clients. (Applies to CometD and Pub/Sub API clients, empApi Lightning components, and event relays only.) **[Add On]** |  50k| 25k | 25k |  |
| Event Publishing: maximum number of event notifications published per hour. (Applies to all publishing methods, including Apex, Pub/Sub API and other APIs, flows, and Process Builder processes.) **[Add On]** |  250k| 250k | 250k |  |

#### High Volume add-on license
This add-on can be purchased multiple times. The add-on is increasing the delivery by :
 
 ##### Delivery
 - +100k Daily (5x 100k = 500k Technical limit)
 - +3M Monthly
 ##### Publishing
 - +25k/hours

 
| Description | Unlimited  | Enterprise | Professional | Essential |
|--|--|--|--|--|
| **Event Delivery**: maximum number of delivered event notifications in the last 24 hours, shared by all clients. (Applies to CometD and Pub/Sub API clients, empApi Lightning components, and event relays only.)| Last 24 hours: **+100k**. Monthly entitlement: **+3M** |  Last 24 hours: **+100k**. Monthly entitlement: **+3M** |  Last 24 hours: **+100k**. Monthly entitlement: **+3M** |  |
|**Event Publishing**: maximum number of event notifications published per hour. (Applies to all publishing methods, including Apex, Pub/Sub API and other APIs, flows, and Process Builder processes.)| **+25k**/hour | **+25k**/hour  |  **+25k**/hour  |  |


### Documentation

1. [Streaming API Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.246.0.api_streaming.meta/api_streaming/intro_stream.htm)
2. [Platform Events Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.platform_events.meta/platform_events/platform_events_intro.htm)