# Core - Reporting

### What are the differents reports available in Salesforce
 - Tabular (no grouping)
 - Summary (grouped by rows)
 - Matrix (grouped by rows and columns)
 - Joined (report blocks that provide differents view of your data)

### Report over Aggregate Data
To display aggregated data, you can use a custom object to represent the incrementation.
If this solution isn't working, it's recommended to use "Tableau/CRM Analytics" and use a "Recipe".

### Display a Map
There is 3 options :
- AppExchange
- LWC with Apex Controller
- Tableau/CRM Analytics (Map is available OTB)


### Reporting over LDV objects
When reporting over LDV records, the timeout limit of 10 minutes need to be taken into consideration and as a best practice, use Tableau/CRM Analytics to report over LDV objects


### Limitations

[See Limitations](../Limitations/ReportingLimits.md)