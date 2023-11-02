[Home](../../README.md)
# Salesforce Shield
Shield Platform Encryption builds on the data encryption options that Salesforce offers out of the box. Data stored in many standard and custom fields and in files and attachments is encrypted using an advanced HSM-based key derivation system. So it’s protected even when other lines of defense are compromised.

## Licenses
Salesforce Shield is provided is provided via an Org License. (No User license)

## Encryption Key
You can use differents key (RSA) to encrypt your data:
- Salesforce Generated Key
- `Bring your own Key (BYOK)`

The BYOK provide a `Cache-Only Key Service` that fetch your key and encrypt on demand without storing the key on Salesforce to avoid any risk.

## Field Encryption Details

### Encryption Types
Salesforce provide different encryption type for each fields and this might impact the way formula, Workflow rules, Duplication rules, etc interact with the data.
- Deterministic Encryption  (✅ Support most cases)
- Probalistic Encryption (❌ limited support)

#### Formula
Encrypted fields are accessible in Formula field so formula fields are still working (With certain [exceptions](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/security_pe_formulas.htm))

## Tradeoffs & Limitations

### Formula, Workflow, Duplicate rules, etc
Salesforce provide different encryption type for each fields and this might impact the way formula, Workflow rules, Duplication rules, etc interact with the data.
- `Deterministic Encryption`  (✅ Support most cases)
- Probalistic Encryption (❌ limited support)

### App Exchange 
App Exchange app need to be evaluated to garanty that the functionalities are still working as expected after the installation of Salesforce Shield.


## Links
[Documentation](https://developer.salesforce.com/docs/atlas.en-us.securityImplGuide.meta/securityImplGuide/security_pe_overview.htm)
