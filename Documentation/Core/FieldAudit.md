[Table of Contents](../Documentation.md)

# Field Audit

Field Audit is a standard functionality that allows the administrator to track up to 20 fields per object in Salesforce.

**Important:** Field history tracking data and Field Audit Trail data do not count against your data storage limits.

Data is accessible for up to 18 months from the UI and 24 months from the API. If needed for a longer period, it's recommended to archive them.

## Field Audit Trail
This add-on stores historical data as Big Objects in Salesforce. Historical data is migrated from related history lists such as Account History into the `FieldHistoryArchive` big object.

With Field Audit Trail, you can increase the amount of fields to track up to 60 fields for up to 10 years.

### Data Retention Policy
The archiving process of historical data is controlled by the `Data Retention Policy`, defining `when` and `how long` the data should be maintained in Salesforce Big Objects.

These two parameters control the Data Retention Policy:
- `Archive after X months`
- `Archive Retention for X years`

### License
Salesforce Field Audit Trail is provided via an Org license for Enterprise and Unlimited editions (no user license required). It's included by default in the `Shield Bundle`.
