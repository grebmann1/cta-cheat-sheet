[Table of Contents](../Documentation.md)

# Flows

## Different Types of Flows Available
- Screen Flow
- Triggered Flow
    - Record-Triggered Flow
    - Scheduled-Triggered Flow
    - Platform Event-Triggered Flow
- Scheduled Path Flow
- Paused Flow

## Flow Considerations
### Scheduled Flow
When implementing a "Scheduled Flow" to run a batch, there is a limitation on the number of rows that can be retrieved per day: `250k` OR `number of user licenses x 200`. If there are more records, it's advisable to consider using `Apex Batch` or an `ETL Process`.

## General Flow Limitations
- Maximum Scheduled Path triggered flows in 24 hours: 250k OR number of user licenses x 200
- Paused Flow: 50k

It is possible to increase these limits by purchasing a `Flow Entitlement Add-on`.
