[Table of Contents](../Documentation.md)

# Integration - Platform Event

### When to Use Platform Event?

1. Real-Time Integration
2. Update External/Internal System with Specific Information/Event
3. Execute Async Flow/Apex with Internal Subscriber
4. Monitor Execution and/or Issues

### How to Publish Platform Event?

1. Flows
2. Processes
3. Apex
4. Salesforce APIs (REST, SOAP, Pub/Sub)

### Data Life

Events are stored in the event bus for `3 days (72h)` for high-volume events. Each event contains a "ReplayId" field that can be used to retrieve the event.
Standard events are now deprecated (Only available for API < 44.0)

### Security

Before delivering a platform event message to a subscribed client, the event payload is decrypted using the encryption key. The platform event message is sent over a secure channel using HTTPS and TLS, ensuring data protection and encryption while in transit.
(Classic Encryption isn't supported; Shield Platform Encryption needs to be enabled)

#### Delivery vs. Publishing

Non-API clients (Apex triggers, Process Builder processes, and flows) don’t count against the event **delivery limit** but toward the **publishing limit**.

#### Limitations & Allocations

| Description | Unlimited | Enterprise | Professional (with API Add-on) | Essential |
|-------------|-----------|------------|------------------------------|-----------|
| Maximum number of concurrent CometD clients (subscribers) across all channels and for all event types. **[Hard Limit]** | `2k` | 1k | 20 |  |
| Maximum number of platform event definitions that can be created in an org | 100 | 50 | 20 |  |
| Maximum number of custom channels that can be created (separate from custom change data capture channels). | 100 | 100 | 100 |  |
| Maximum number of distinct platform events that can be added to a channel as part of channel members. | `50` | 50 | 5 |  |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours (shared by all clients). **[Add On]** | `50k` | 25k | 25k |  |
| Event Publishing: maximum number of event notifications published per hour. **[Add On]** | `250k` | 250k | 250k |  |

### High Volume Add-on License

This add-on can be purchased multiple times, increasing delivery by:

| Description | Unlimited | Enterprise | Professional | Essential |
|-------------|-----------|------------|--------------|-----------|
| **Event Delivery**: maximum number of delivered event notifications in the last 24 hours (shared by all clients). | Last 24 hours: `+100k`. Monthly entitlement: `+3M` | Day: **+100k**. Month: **+3M** | Day: **+100k**. Month: **+3M** |  |
| **Event Publishing**: maximum number of event notifications published per hour. | `+25k`/hour | **+25k**/hour | **+25k**/hour |  |


