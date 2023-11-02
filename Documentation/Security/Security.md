[Home](../../README.md)
# Security
Salesforce is built with security to protect your data and applications. You can also implement your own security scheme to reflect the structure and needs of your organization. Protecting your data is a joint responsibility between you and Salesforce. The Salesforce security features enable you to empower your users to do their jobs safely and efficiently.

## Data Encryption

With Shield Platform Encryption, you can encrypt a variety of widely used standard fields, along with some custom fields and many kinds of files.\
**Shield Platform Encryption** also supports person accounts, cases, search, approval processes, and other key Salesforce features.\
**Classic encryption** lets you protect only a special type of custom text field, which you create for that purpose.

[go to Salesforce Shield](../Product%20&%20Clouds/addOn_SalesforceShield.md)

| Feature| Classic Encryption| Platform Encryption|
|--|--|--|
| Pricing| Included in base user license | Additional fee applies |
| Encryption at Rest| ✅| ✅|
| Native Solution (No Hardware or Software Required)  | ✅| ✅|
| Encryption Algorithm| 128-bit Advanced Encryption Standard (AES) | 256-bit Advanced Encryption Standard (AES) |
| HSM-based Key Derivation| |✅|
| Manage Encryption Keys Permission| |✅|
| Generate, Export, Import, and Destroy Keys| ✅| ✅|
| PCI-DSS L1 Compliance | ✅| ✅|
| Masking| ✅|
| Mask Types and Characters  | ✅|
| View Encrypted Data Permission Required to Read Encrypted Field Values | ✅ | 
| Encrypted Standard Fields| |✅|
| Encrypted Attachments, Files, and Content|| ✅|
| Encrypted Custom Fields| `Dedicated custom field type, limited to 175 characters` | ✅ |
| Encrypt Existing Fields for Supported Custom Field Types | |✅|
| Search (UI, Partial Search, Lookups, Certain SOSL Queries) | |✅|
| API Access| ✅| ✅|
| Available in Workflow Rules and Workflow Field Updates || ✅|
| Available in Approval Process Entry Criteria and Approval Step Criteria || ✅ |


Salesforce is also providing an Add-On called `Salesforce Data Mask` to mask confidential or protected information, such as personally identifiable information (PII), when deploying **sandbox** environments.

Data masking isn't an OTB solution working in Production so if you want to simulate something like *****1234 then you should use a formula or even store the information like that.

## Audit & Monitor
### OTB
Salesforce provide some monitoring features OTB :
- User Login Monitoring
- Field History Tracking

### Salesforce Shield
Salesforce shield provide event monitoring capability to monitor detailed performance, security, and usage accross the Salesforce org.\
Shield track `login history`, `transaction security`, and `event logs`.\
Each interaction is tracked and accessible via the API. The monitoring data can be imported to Tableau or Splunk.

## Compliance
Salesforce provide the `Field Metadata Category` that allow the administrator to mark fields with specific information in the object settings.
- Conpliance Categorization
- Data Owner
- Data Sensibility Lvel
    - Public
    - Internal
    - Confidential
    - Restricted
    - Mission Critical

Salesforce has a list of regulatory and security compliance certifications for it's core platform and core products:
- CCPA - California consumer Privacy Act
- COPPA - Children's Online Privacy protection Act
- GDPR - General Data Protection Regulation
- HIPAA - Health Insurance Portability and Accountability Act
- PCI - Payment Card Industry
- PersonalInfo - Personal Information
- PII - Personally Identifiable Information

### PCI - Payment Card Industry
It's an industry standard that need to be followed.

These informations **need** to be encrypted:
- Card Holder Information
- Card Number
- Card Expiration Date

These information **can't** be stored.
- Pin (Even encrypted)
- CVV/CVC
- Authentication Data

In case you want to store it using `Salesforce Standard`, then you should only store the `Token` provided by the payment gateway. Storing only the payment token is compliant !
