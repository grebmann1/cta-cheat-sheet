[Table of contents](../Documentation.md)
# Document Generation

It's important to consider an external solution to improve the user experience. Basic email template is Salesforce are good for simple emails.

## Conga Composer
Conga is currently the leader for document generation in Salesforce with their product Conga Composer. (They also support e-signature).
1. [Conga Composer Website](https://conga.com/products/conga-composer)
2. [Conga Composer Documentation](https://documentation.conga.com/composer/october-23/salesforce/conga-composer-193694433.html)

#### Features
- Create easily documents in different formats (Word, Excel, Pdf, etc)
- Documents can be directly stored in Salesforce or externaly (AWS, Google, etc)
- Templating directly from (Word, Excel, etc)
- Delivery method includes
    - Send Email, Printing
    - Save as Note & Attachments
    - Conga Sign, Docusign, Adobe Signature, Conga Contracts
- Extension
    - eSignature
    - Conga Trigger
    - Conga Batch

#### Integration
 - Files are created in Conga servers using REST API
 - Files and Templates are stored in Salesforce as Custom objects
 - Salesforce Mobile App Supported (with a Conga Connected App)
 - Document created can be launched from 
    - Conga Composer Button (using formula)
    - Flow (Add-on with Conga Trigger)
    - Apex (Using Conga API)
 - Custom Objects are used to represent the solution
    - Conga Email Template (To store the email template)
    - Conga Query Manager (To store the queries for the document generation)