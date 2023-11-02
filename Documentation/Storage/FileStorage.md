[Home](../../README.md)
# File Storage 

## File Storage Allocation

All orgs are allocated `10GB for file storage by default.`

File storage = `10GB + number of licenses * license allocations + Extra add-ons`


## File Limitations
Files size are limited to 2GB.
Files that are attached to articles in Lightning Knowledge : 5MB
Files can only be shared 2K times.
File connect can be used to use file from Google Drive, Dropbox, etc

## When to look for an external Solution ?
- Streaming video.
- Very large files (more than 2GB).
- Files already available in an external tool.


## File Storage by Salesforce Edition

|SALESFORCE EDITION|FILE STORAGE ALLOCATION PER ORG|FILE STORAGE ALLOCATION PER USER LICENSE| 
|--|--|--|
| Professional  | 10 GB  | 612MB
| Enterprise    | 10 GB  | 2GB 
| Performance   | 10 GB  | 2GB
| Unlimited     | `10 GB`  | `2GB`
| Developer     | 20 MB   | N/A


## File Connect (External Data Storage)
With Files Connect, Salesforce users can access, share, and search external data from systems like `Quip`, `Google Drive`, `SharePoint`, or `Box`.

Be aware, File Connect isn't made to replace "Attachement". It's only to access Personnal files and share it.


## External Data Storage with App Exchange

### List of Solutions (Sample)
This is a non exhaustive list of solutions available in App Exchange.
- S-Drive `Recommended`
- CloudFiles
- S3-link | Amazon Connector




## S-Drive (Recommended Solution)
 External tool available in App Exchange

### Storage
 S-Drive is using Amazon S3 to store the data.

### Key Features
 - File management, Microsoft format editor
 - E-Signature with DocuSign
 - Tooling API for migration
 - Salesforce Sharing model

### Migration
 Migration can be done using their tooling API to migrate the files in Amazon S3 and link them to Salesforce records.


