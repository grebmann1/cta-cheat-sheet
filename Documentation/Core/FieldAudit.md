[Table of contents](../Documentation.md)
# Field Audit

Field Audit is a standard functionallity that allow the administrator to set up to `20 fields per objects to be tracked` in Salesforce.

**Important:** Field history tracking data and Field Audit Trail data don’t count against your data storage limits.

`Data are accessible for up to 18 months from the UI and 24 months from the API` so if it's needed to have them stored for a longer period, it's recommended to archive them.

## Field Audit trail
This add-on is storing the historical data as Big Ojects in salesforce.
Historical Data are migrated from related history lists such as Account History into
the `FieldHistoryArchive` big object.

With Field Audit trail, you can increase the amount of fields to track to `up to 60 fields` for up to `10 Years`.



### Data Retention Policy
The archiving process of the historical data is controlled by the `Data Retention Policy` that define `When` and `How long` the data should be maintained in salesforce Big Objects.

These 2 parameters control the Data Retention Policy:
- `Archive after X months`
- `Archive Retention for X years`

### License
Salesforce Field Audit Trail is provided via an Org license for Enterprise and Unlimited edition.(No User license).\
It's included by default in the `Shield Bundle`

