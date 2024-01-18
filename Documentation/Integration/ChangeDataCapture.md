[Table of Contents](../Documentation.md)

# Integration - CDC (Change Data Capture)

### When to Use CDC?

1. Real-Time Integration
2. Update External System When Change Occurs

### Custom Channels

Custom Channels are used to group events together and filter events to provide more granular control.
[Custom Channels are only configurable with **Metadata API**]

### Enriched Fields

Enriched fields are used to include "Extra Fields" in the events that are published.
For CDC, enriched fields are available for "Update" and "Delete." Up to 10 enriched fields can be included by channel members. (For a custom channel including Account and Contact, this would mean 2x 10 enriched fields).
[Enriched fields are only configurable with **Metadata API**]

### Filter Event

Events can be filtered using SOQL queries to provide more granular control over the events published to the subscribers. (Useful for reducing the number of events published)

### Security

If Salesforce record fields are encrypted with **Shield Platform Encryption**, changes in encrypted field values generate change events. To ensure the events are encrypted (not in clear text), an **event bus tenant secret** needs to be created, and encryption enabled.

Before delivering a platform event message to a subscribed client, the event payload is decrypted using the encryption key. The platform event message is sent over a secure channel using HTTPS and TLS, ensuring data protection and encryption while in transit.
(Classic Encryption isn't supported; Shield Platform Encryption needs to be enabled)

### Data Life

Events are stored in the event bus for `3 days (72h)`. Each event contains a "ReplayId" field that can be used to retrieve the event.

#### Limitations & Allocations

| Description | Enterprise | Unlimited |
|-------------|------------|-----------|
| Maximum number of concurrent CometD clients (subscribers) across all channels and for all event types. **[Hard Limit]** | 1K | `2K` |
| Maximum number of entities for Change Data Capture on the default standard channel or a custom channel. **[Add On]** | 5 | 5 |
| Maximum number of custom channels. **[Add On]** | 100 | 100 |
| Maximum number of entities selected for Change Data Capture across channels. **[Add On]** | 5 | 5 |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours, shared by all clients. **[Add On]** | 25k | `50k` |

There is `No Publishing Limits`on CDC as this can't be controlled by Salesforce.

#### Change Data Capture Add-on License

This add-on can be purchased multiple times. It increases delivery by:

- `100k Daily (5x 100k = 500k Technical Limit / add on license)`
- `3M Monthly`

| Description | Enterprise | Unlimited |
|-------------|------------|-----------|
| Maximum number of entities for Change Data Capture on channels | No Limit | `No Limit` |
| Event Delivery: maximum number of delivered event notifications in the last 24 hours, shared by all clients | Day: **+100k**. Month: **+3M** | Day: `+100k`. Month: `+3M` |

### Documentation

1. [Change Data Capture Developer Guide](https://developer.salesforce.com/docs/atlas.en-us.change_data_capture.meta/change_data_capture/cdc_intro.htm)
