[Table of Contents](../Documentation.md)

# Limitations - Bulk APIs

### Batch Allocations
You can submit up to 15,000 batches per rolling 24-hour period. This allocation is shared between Bulk API and Bulk API 2.0, so every batch that is processed in Bulk API or Bulk API 2.0 counts towards this allocation.

In Bulk API 2.0, batches are created for you automatically. In Bulk API, you must create the batches yourself.

### Bulk API 1.0 vs 2.0
- 2.0 supports `automatic retry of failed records`.
- 2.0 support `Automatic parallel processing` (Best way to justify 2.0).
- 2.0 has `Higher concurrency limits`.

### General Limits
| Item | Bulk API Limit | Bulk API 2.0 Limit |
|--|--|--|
| Batch and job lifespan | See details in content | See details in content |
| Binary content | See details in content | N/A |
| Maximum time that a job can remain open | 24 hours | 24 hours (applies to ingest jobs, not query jobs) |

### Limits Specific to Ingest Jobs
| Item | Bulk API Limit | Bulk API 2.0 Limit |
|--|--|--|
| Maximum number of records uploaded per 24-hour rolling period | 150M | 150M |
| Batch processing time | See details in content | Same as Bulk API |
| Maximum time before a batch is retried | 5 minutes | Automatically handled by the API |
| Maximum file size | 10 MB per batch | 150 MB per job |
| Maximum number of characters in a field | 131,072 | Same as Bulk API |
| Maximum number of fields in a record | 5k | Same as Bulk API |
| Maximum number of characters in a record | 400k | Same as Bulk API |
| Maximum number of records in a batch | 10k | N/A |
| Maximum number of characters for all the data in a batch | 10M | N/A |

### Documentation
There might be a link or source where you want to direct users for further details.
