[Table of contents](../Documentation.md)
# Flows

## Differents type of Flows available
- Screen Flow
- Triggered Flow
    - Record - Triggered Flow
    - Scheduled - Triggered Flow
    - Platform Event - Triggered Flow
- Scheduled Path Flow
- Paused Flow


## Flows consideration
### Scheduled Flow
When doing a "Scheduled Flow" to run a batch, there is a limitation of rows that can be retrieved per day: `250k` OR `number of user licenses x 200`.
If there is more records, it's better to consider `Apex Batch` or an `ETL Process`.


## General Flow Limitations
 
- Max Scheduled Path triggered flow in 24h:  250k OR number of user licenses x 200
- Paused Flow: 50k

It's possible to increase the limits by buying an `Flow Entitlement Add-on`.