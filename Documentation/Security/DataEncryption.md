[Table of Contents](../Documentation.md)

# Data Encryption 

## Classic vs Platform Encryption

**Shield Platform Encryption** offers encryption for widely used standard fields, certain custom fields, and various file types. It supports person accounts, cases, search, approval processes, and other critical Salesforce features. 

**Classic Encryption**, on the other hand, focuses solely on a specific type of custom text field created for that purpose.

The Add-on [Platform Encryption](../Product%20&%20Clouds/addOn_ShieldPlatformEncryption.md) can be purchased to extend the standard functionalities.

| Feature | Classic Encryption | Platform Encryption |
|--|--|--|
| Pricing | Included in base user license | Additional fee applies |
| Encryption at Rest | ✅ | ✅ |
| Native Solution (No Hardware or Software Required) | ✅ | ✅ |
| Encryption Algorithm | 128-bit Advanced Encryption Standard (AES) | 256-bit Advanced Encryption Standard (AES) |
| HSM-based Key Derivation | | ✅ |
| Manage Encryption Keys Permission | | ✅ |
| Generate, Export, Import, and Destroy Keys | ✅ | ✅ |
| PCI-DSS L1 Compliance | ✅ | ✅ |
| Masking | ✅ |
| Mask Types and Characters | ✅ |
| View Encrypted Data Permission Required to Read Encrypted Field Values | ✅ |
| Encrypted Standard Fields | | ✅ |
| Encrypted Attachments, Files, and Content | | ✅ |
| Encrypted Custom Fields | `Dedicated custom field type, limited to 175 characters` | ✅ |
| Encrypt Existing Fields for Supported Custom Field Types | | ✅ |
| Search (UI, Partial Search, Lookups, Certain SOSL Queries) | | ✅ |
| API Access | ✅ | ✅ |
| Available in Workflow Rules and Workflow Field Updates | | ✅ |
| Available in Approval Process Entry Criteria and Approval Step Criteria | | ✅ |

## Data Masking

Salesforce Data Mask stands as a robust data security tool tailored for Salesforce administrators and developers. Rather than manually securing data and managing access in sandbox orgs, Data Mask automates the data masking process within these environments. This powerful tool empowers admins and developers to obfuscate sensitive information such as Personally Identifiable Information (PII) or sales revenue seamlessly.

Data masking is not available as an out-of-the-box solution for Production environments. If needed, information can be simulated like *****1234 using formulas or storage methods.

This solution covers a wide spectrum of Salesforce offerings, including 
- Sales Cloud
- Service Cloud
- Work.com
- Salesforce's Industry products
- AppExchange applications and platform customizations.

Leveraging platform-native obfuscation technology, Data Mask ensures the masking of sensitive data in both full and partial sandboxes. Admins have the flexibility to apply `varying levels of masking based on the sensitivity of the information`. Once the data undergoes masking in a sandbox, the process is irreversible, guaranteeing that the data cannot be reversed to a readable or identifiable state in any other environment. It's important to note that this safeguarding process does not impact production data. Should the need arise, admins can always refresh the sandbox data from the production environment, creating a new sandbox org.

This tool provides configurable options to handle different levels of masking, depending on the data sensitivity:

- Replace private data in sandboxes with random characters.
- Substitute private data with mapped words following a similar context.
- Apply pattern-based masking to mask private data.
- Option to delete sensitive data altogether.

Data mask is free to use and can be installed as a managed package [Package Link](https://sfdc.co/datamask-install)

