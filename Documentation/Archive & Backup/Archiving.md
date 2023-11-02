[Home](../../README.md)
# Archiving

## Different Archiving Stategies

When archiving, you should decide if you store the data in Salesforce `Big Objects` or outside Salesforce in an Database or DataLake.

## Archive LDV records
It's important to archive LDV records to avoid degrading the performance of your orgs.


## Salesforce Solution
No Specific salesforce product but solutions can be found on App Exchange to archive data from Salesforce in Big Objects and make them available via LWC components.

## External Solution
Solutions such as `Own Backup` are ideal to manage archiving schedules and store the data in Amazon S3.


# Backup Solution
## Salesforce Solution - Salesforce Backup
Salesforce is providing a solution called `Salesforce Backup` that can be used to manage Backup directly from Salesforce and control the schedule of backups.\
Data are stored in AWS and migrated there using the `Bulk API `(Web Server flow))

![Salesforce Backup](../../Images/CTA%20-%20Diagrams%20-%20Salesforce%20Backup.png)

## External Solution
Solutions such as `Own Backup` are ideal to manage archiving schedules and store the data in Amazon S3.\
`Own Backup` is available in App Exchange.


