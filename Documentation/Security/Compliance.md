[Table of Contents](../Documentation.md)

# Compliance

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

## PCI - Payment Card Industry

It's an industry standard that mandates encryption for:
- Cardholder Information
- Card Number
- Card Expiration Date

Certain information should not be stored, including:
- Pin (Even encrypted)
- CVV/CVC
- Authentication Data

If using `Salesforce Standard` for storage, only the `Token` provided by the payment gateway should be stored to be compliant.
