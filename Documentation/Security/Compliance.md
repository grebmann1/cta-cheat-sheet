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

## Privacy Center

Salesforce Privacy Center is an essential tool for organizations looking to streamline their privacy management practices and maintain compliance with data protection regulations.\
By leveraging its features for data mapping, privacy request management, and compliance documentation, businesses can enhance their privacy operations and build trust with their customers.

![Privacy Center](/Images/privacyCenter_1.png)

1. **Data Mapping and Inventory**
The Privacy Center enables organizations to create a comprehensive inventory of the personal data they process. This feature assists in mapping data flows across the organization, providing visibility into how personal data is collected, stored, used, and shared.

2. **Privacy Request Management**
Organizations can automate the handling of individual rights requests, such as access, deletion, and data portability, directly from the Privacy Center. This streamlines the process of responding to requests within the legally mandated timeframes, ensuring compliance with regulations.

3. **Assessment and Documentation**
Privacy Center aids in conducting privacy impact assessments (PIAs) and data protection impact assessments (DPIAs) to evaluate privacy risks associated with data processing activities. It also facilitates the documentation of these assessments, helping organizations maintain records of their compliance efforts.

4. **Integration with Salesforce Products**
Seamlessly integrated with various Salesforce products, the Privacy Center enhances data management and privacy practices across the Salesforce ecosystem, including Sales Cloud, Service Cloud, Marketing Cloud, and more.

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
