[Table of Contents](../Documentation.md)

# Document Generation

Enhancing the user experience often necessitates considering an external solution. While basic email templates in Salesforce suffice for simple emails, more comprehensive solutions can significantly improve document generation processes.

## Conga Composer

Conga Composer stands as the leading document generation tool within Salesforce, offering robust document generation capabilities and supporting e-signatures.

1. [Conga Composer Website](https://conga.com/products/conga-composer)
2. [Conga Composer Documentation](https://documentation.conga.com/composer/october-23/salesforce/conga-composer-193694433.html)

### Key Features

- Effortlessly create documents in various formats (Word, Excel, PDF, etc.).
- Directly store documents in Salesforce or external platforms (AWS, Google, etc.).
- Use templates from applications like Word and Excel.
- Delivery options include:
    - Sending emails and printing
    - Saving as Note & Attachments
    - Using eSignature tools like Conga Sign, Docusign, Adobe Signature, and Conga Contracts
- Extensions available:
    - eSignature
    - Conga Trigger
    - Conga Batch

### Integration

- Files are generated on Conga servers using REST API.
- Files and Templates are stored in Salesforce as Custom objects.
- Supported in the Salesforce Mobile App (requires a Conga Connected App).
- Documents can be created from:
    - Conga Composer Button (using formula)
    - Flow (Add-on with Conga Trigger)
    - Apex (using Conga API)
- Custom Objects used in the solution include:
    - Conga Email Template (to store email templates)
    - Conga Query Manager (to store queries for document generation)
