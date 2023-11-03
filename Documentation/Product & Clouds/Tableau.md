[Table of contents](../Documentation.md)
# Tableau Products
Tableau is a tool that drive intelligent predictions and recommendations across your analytics to power data-driven action.

## Integration with Salesforce (Exclusive)
Tableau is known as `CRM Analytics` in Salesforce as it provide Tableau features directly inside Salesforce.

## Licenses

|License| Description|
|--|--|
|Tableau Creator| Connect your data, build vizzes, and publish dashboards in Tableau Desktop.|
|Tableau Explorer| Edit existing dashboards. Available for teams and organizations.|
|Tableau Viewer|Access existing dashboards. Available for teams and organizations.|

![Products](../../Images/CTA%20-%20Diagrams%20-%20Tableau%20-%20Products.png)


## When to choose between Tableau and CRM Analytic
![Tableau vs CRM Analytics](../../Images/CTA%20-%20Diagrams%20-%20Tableau%20-%20Choice.png)

# CRM Analytics
CRM Analytics is using a specific connector that was designed to connect Salesforce and Tableau.

CRM Analytics is available in the **Salesforce mobile app** or with the unique CRM Analytics app.

## Licenses
|License| Description|
|--|--|
|CRM Analytics Growth| Basic, provide `100M` rows/License
|CRM Analytics Plus| Provide more data `1B` rows/License

For External users, you need to assign the `CRM Analytics for Communities` permission set license.

## CRM Analytics Limits

| BASELINE ROW ALLOCATION   | ALLOCATED ROWS |
|----------------------------------------------------|----------------------|
| CRM Analytics Plus|`10 billion`|
| CRM Analytics Growth| `100 million`|
| Sales Analytics| 25 million|
| Service Analytics| 25 million|
| Event Monitoring Analytics| 50 million|
| B2B Marketing Analytics| 25 million|
| CRM Analytics for Financial Services Cloud| 25 million|
| CRM Analytics for Health Cloud| 25 million|
| Extra Data Rows license| `100 million`|

##### Note
When using a Salesforce local input connection, `CRM Analytics bulk API usage doesn’t count towards Salesforce bulk API limits`.\
Use of the external Salesforce connection and output connection impacts your limits.\
The dataflow submits a separate bulk API call to extract data from each Salesforce object. The dataflow uses a batch size of 100,000–250,000, depending on whether the dataflow or the bulk API chunks the data.\
As a result, to extract 1 million rows from an object, the dataflow creates 4–10 batches.



## Connect and Sync Your Data to CRM Analytics

CRM Analytics connectors give you an easy way to connect data inside and outside of Salesforce with CRM Analytics.\
CRM Analytics provides a prebuilt connector for data in your local org and a range of configurable connectors for remote data in external Salesforce orgs, apps, data warehouses, and database services.

![Data Sync](../../Images/CTA%20-%20Diagrams%20-%20Tableau%20-%20Data%20Sync.png)

Example of Salesforce Connector :
- Salesforce External Connection
- Salesforce Marketing Cloud Connection
- Tableau Online Connection
- Database connections
- Heroku Postgres
- SAP HANA
- etc

## Data access and visibility
If a CRM Analytics user has access to a dataset, the user has access to all records in the dataset by default.\
To restrict access to records, you can `implement row-level security on a dataset when you use sharing inheritance and security predicates`. Sharing inheritance automatically applies a Salesforce object’s sharing logic to the dataset’s rows.\
A security predicate is a manually assigned filter condition that defines dataset row access.

### Schedule, Run, and Monitor Data Sync
In CRM Analytics, you can schedule sync to run automatically, manually run a sync, and monitor a sync's progress, all in the data manager.

##### Note
If you have a `CRM Analytics Plus license`, you can set the schedule to `run every 5, 15, 20, or 30 minutes`. 



## Data Manager
The data manager is where you monitor your data jobs, prepare datasets with recipes and dataflows, and connect to data.

| TAB | USAGE|
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| Jobs Monitor   | Monitor and troubleshoot jobs, like recipes that are currently running.|
| Data Assets| View data sources, including datasets and connected objects, that you can use in recipes. Upload CSV files to get access to other data sources that don't have prebuilt connectors. |
| Recipes   | View, edit, delete, and run recipes. You can also access Data Prep to create a recipe from this tab.|
| Usage| Monitor Data Pipeline usage and limits. You can also view this information on the Getting Started page in setup. The limits vary based on your licenses. |
| Connections| Create, edit, and delete connections to different source and target systems. A connection enables recipes to access data in that system. Data Pipelines provides out-of-the-box connectors that allow you to quickly create connections. |
| Data Templates | Create common use case data tasks from templates to accelerate your data pipeline experience.  |


![Data Manager](../../Images/CTA%20-%20Diagrams%20-%20Tableau%20-%20Data%20Manager.png)



