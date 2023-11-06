[Table of contents](../Documentation.md)
# Limitations - APEX Governor Limits

### Per-Transaction Apex Limits
`These limits count for each Apex transaction`. For Batch Apex, these limits are reset for each execution of a batch of records in the execute method.

| Description| Synchronous Limit | Asynchronous Limit|
|--|--|--|
| Total number of SOQL queries issued | 100| 200|
| Total number of records retrieved by SOQL queries| `50k`| `50k`|
| Total number of records retrieved by Database.getQueryLocator| 10k| 10k|
| Total number of SOSL queries issued | 20| 20 |
| Total number of records retrieved by a single SOSL query| `2k`| `2k` |
| Total number of DML statements issued| 150| 150|
| Total number of records processed as a result of DML statements| 10k| 10k|
| Total stack depth for any Apex invocation that recursively fires triggers due to insert, update, or delete statements | 16 | 16 |
| Total number of callouts (HTTP requests or web services calls) in a transaction | 100 | 100 |
| Maximum cumulative timeout for all callouts (HTTP requests or Web services calls) in a transaction | 120 seconds | 120 seconds |
| Maximum number of methods with the future annotation allowed per Apex invocation | 50 | 0 in batch and future contexts; 50 in queueable context |
| Maximum number of Apex jobs added to the queue with System.enqueueJob | 50 | 1 |
| Total number of sendEmail methods allowed | 10 | 10 |
| Total heap size4 | 6 MB | 12 MB |
| Maximum CPU time on the Salesforce servers | 10 seconds | 60 seconds |
| Maximum execution time for each Apex transaction | 10 minutes | 10 minutes |
| Maximum number of push notification method calls allowed per Apex transaction | 10 | 10 |
| Maximum number of push notifications that can be sent in each push notification method call | 2k | 2k |
| Maximum number of EventBus.publish calls for platform events configured to publish immediately | 150 | 150 |
