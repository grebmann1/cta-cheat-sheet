# Limitations - Bulk Apis 

### Batch Allocations
You can submit up to 15,000 batches per rolling 24-hour period. This allocation is shared between Bulk API and Bulk API 2.0, so every batch that is processed in Bulk API or Bulk API 2.0 counts towards this allocation.

In Bulk API 2.0, batches are created for you automatically. In Bulk API, you must create the batches yourself.

### Bulk API 1.0 vs 2.0
- 2.0 support autmatic retry of failed records
- 2.0 Support parallel processing

### General Limits
| Item | Bulk API Limit| Bulk API 2.0 Limit|
|--|--|--|
| Batch and job lifespan | Batches and jobs that are older than seven days are removed from the queue if batches are in a terminal state (completed, aborted, or failed), regardless of their respective job status. The seven days are measured from the youngest batch associated with a job, or the age of the job if there are no batches. You can't create batches associated with a job that is more than 24 hours old. Batches in a non-terminal state that are older than seven days are periodically cleaned up with their respective jobs. | Jobs in a terminal state (completed, aborted, or failed) that are older than seven days are deleted. Jobs in a non-terminal state that are older than seven days are periodically cleaned up. |
| Binary content | - The length of any file name can't exceed 512 bytes. - A zip file can't exceed 10 MB. - The total size of the unzipped content can't exceed 20 MB. - A maximum of 1k files can be contained in a zip file. Directories don't count toward this total. | N/A |
| Maximum time that a job can remain open | 24 hours | The same. (But this only applies to ingest jobs, not query jobs.) |


### Limits Specific to Ingest Jobs
| Item                                           | Bulk API Limit                                                                                    | Bulk API 2.0 Limit                                              |
|------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| Maximum number of records uploaded per 24-hour rolling period | 150M (15k batches x 10k records per batch maximum) | 150M                                                   |
| Batch processing time | Batches are processed in chunks. The chunk size depends on the API version. In API version 20.0 and earlier, the chunk size is 100 records. In API version 21.0 and later, the chunk size is 200 records. If it takes longer than 5 minutes to process a whole batch, the Bulk API places the remainder of the batch back in the queue for later processing. If the Bulk API continues to exceed the 5-minute limit on subsequent attempts, the batch is placed back in the queue and reprocessed up to 20 times before the batch is permanently marked as failed. | Same as Bulk API |
| Maximum time before a batch is retried | 5 minutes | The API automatically handles retries. If you receive a message that the API retried more than 20 times, use a smaller upload file and try again. |
| Maximum file size | 10 MB per batch | 150 MB per job |
| Maximum number of characters in a field| 131,072| Same as Bulk API|
| Maximum number of fields in a record | 5k | Same as Bulk API|
| Maximum number of characters in a record| 400k | Same as Bulk API|
| Maximum number of records in a batch| 10k| N/A|
| Maximum number of characters for all the data in a batch | 10M| N/A|

