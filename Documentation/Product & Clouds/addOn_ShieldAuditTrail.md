[Table of Contents](../Documentation.md)

# Field Audit Trail

Field Audit Trail  in Salesforce is a feature designed to track changes made to specific fields within standard and custom objects over a defined period. It extends Salesforce's standard functionality by offering an extended historical view of data modifications, providing valuable insights into data changes and maintaining a comprehensive audit trail for compliance and security purposes.

## Licenses
Salesforce Field Audit Trail is provided via an `Platform License` (No User license).
- Salesforce Payments External
- Salesforce Payments Internal

## Field Audit Trail
This add-on stores historical data as Big Objects in Salesforce. Historical data is migrated from related history lists such as Account History into the `FieldHistoryArchive` big object.

With Field Audit Trail, you can increase the amount of fields to track up to 60 fields for up to 10 years.

### Data Retention Policy
The archiving process of historical data is controlled by the `Data Retention Policy`, defining `when` and `how long` the data should be maintained in Salesforce Big Objects.

These two parameters control the Data Retention Policy:
- `Archive after X months`
- `Archive Retention for X years`

### License
Salesforce Field Audit Trail is provided via an `Platform license` for Enterprise and Unlimited editions (no user license required). It's included by default in the `Shield Bundle` but can be bought separatly as an add-on.
