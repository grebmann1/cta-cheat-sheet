[Table of contents](../Documentation.md)

# Security

Salesforce is designed with robust security measures to safeguard your data and applications. You have the flexibility to implement your own security scheme tailored to your organization's structure and requirements. Protecting your data is a collaborative responsibility between your organization and Salesforce. The platform's security features empower users to perform their tasks securely and efficiently.

## Data Encryption

Shield Platform Encryption offers encryption for widely used standard fields, certain custom fields, and various file types. It supports person accounts, cases, search, approval processes, and other critical Salesforce features. Classic encryption, on the other hand, focuses solely on a specific type of custom text field created for that purpose.

Explore more about [Salesforce Shield](../Product%20&%20Clouds/addOn_SalesforceShield.md)

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

Salesforce also provides an Add-On known as `Salesforce Data Mask` to mask confidential information, like personally identifiable information (PII), when deploying sandbox environments.

Data masking is not available as an out-of-the-box solution for Production environments. If needed, information can be simulated like *****1234 using formulas or storage methods.

## Audit & Monitoring

### Out-of-the-Box (OTB)

Salesforce offers some monitoring features such as:
- User Login Monitoring
- Field History Tracking

### Salesforce Shield

Salesforce Shield enhances monitoring capabilities by providing detailed performance, security, and usage tracking across the Salesforce org. It tracks `login history`, `transaction security`, and `event logs`. Each interaction is tracked and accessible via the API, and the monitoring data can be imported into Tableau or Splunk.

## Compliance

Salesforce introduces the `Field Metadata Category` allowing administrators to tag fields with specific information in object settings, including:
- Compliance Categorization
- Data Owner
- Data Sensibility Level
  - Public
  - Internal
  - Confidential
  - Restricted
  - Mission Critical

Salesforce holds various regulatory and security compliance certifications for its core platform and products, including:
- CCPA - California Consumer Privacy Act
- COPPA - Children's Online Privacy Protection Act
- GDPR - General Data Protection Regulation
- HIPAA - Health Insurance Portability and Accountability Act
- PCI - Payment Card Industry
- PersonalInfo - Personal Information
- PII - Personally Identifiable Information

### PCI - Payment Card Industry

It's an industry standard that mandates encryption for:
- Cardholder Information
- Card Number
- Card Expiration Date

Certain information should not be stored, including:
- Pin (Even encrypted)
- CVV/CVC
- Authentication Data

If using `Salesforce Standard` for storage, only the `Token` provided by the payment gateway should be stored for compliance.
