[Table of contents](../Documentation.md)

# Salesforce Shield

Shield Platform Encryption enhances the data encryption options provided by Salesforce. It encrypts data stored in many standard and custom fields, files, and attachments using an advanced HSM-based key derivation system, ensuring protection even when other lines of defense are compromised.

## Licenses
Salesforce Shield is provided via an Org License (No User license).

## Encryption Key
Different RSA keys can be used to encrypt data:
- Salesforce Generated Key
- Bring Your Own Key (BYOK)

BYOK provides a Cache-Only Key Service that fetches your key and encrypts data on demand without storing the key on Salesforce to mitigate any risks.

## Field Encryption Details

### Encryption Types
Salesforce offers different encryption types for each field, impacting interactions with data in formulas, Workflow rules, Duplication rules, etc:
- Deterministic Encryption (✅ Supports most cases)
- Probabilistic Encryption (❌ Limited support)

#### Formula
Encrypted fields remain accessible in Formula fields; however, there are certain [exceptions](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/security_pe_formulas.htm) to consider.

## Trade-offs & Limitations

### Formula, Workflow, Duplicate rules, etc
Different encryption types for fields may affect interactions with data in Formula, Workflow rules, Duplication rules, etc:
- Deterministic Encryption (✅ Supports most cases)
- Probabilistic Encryption (❌ Limited support)

### App Exchange
App Exchange apps need evaluation to ensure their functionalities remain intact after the installation of Salesforce Shield.

## Links
[Documentation](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/security_pe_overview.htm)
