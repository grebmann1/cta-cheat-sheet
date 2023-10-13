# Storage - File Storage 

### File Storage Allocation

All orgs are allocated 10GB for file storage by default

File storage = 10GB + number of licenses * license allocations + **Extra add-ons**


### File Limitations
Files size are limited to 2GB.
Files that are attached to articles in Lightning Knowledge : 5MB
Files can only be shared 2K times.
File connect can be used to use file from Google Drive, Dropbox, etc


### File Storage by Salesforce Edition

| SALESFORCE EDITION    | FILE STORAGE ALLOCATION PER ORG | FILE STORAGE ALLOCATION PER USER LICENSE | 
|--|--|--|
| Professional          | 10 GB  | 612MB
| Enterprise            | 10 GB  | 2GB 
| Performance           | 10 GB  | 2GB
| Unlimited             | 10 GB  | 2GB
| Developer             | 20 MB   | N/A


# External solution to provide File Storage

## Salesforce Connect
 With Files Connect, Salesforce users can access, share, and search external data from systems like Quip, Google Drive, SharePoint, or Box.

 Files from external repositories, like Google Docs and Microsoft® SharePoint®, are available only if Salesforce Files Connect is configured in your organization and enabled for you.

## S-Drive
 External tool to store file to has capabilities to stream and read video.
### Architecture
 S-Drive is using Amazon S3.
#### PRO
 - File management, Microsoft format editor
 - E-Signature with DocuSign
 - Tooling API for migration
 - Salesforce Sharing model

#### Usage
 - Replace “Salesforce Files Connect” when we need more than Box, Google Drive or Sharepoint

#### Migration
  TBD !

#### Similar tools available in AppExchange
 - Drive Connect
 - CloudFiles | Document management
 - S3-link | Amazon Connector

