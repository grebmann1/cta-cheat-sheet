[Table of Contents](../Documentation.md)

# Data Migration

During data migration, following this flow is recommended:

1. **Data Extraction & Data Cleaning**
    - Connect the system to your ETL (Extract, Transform, Load) tool.
    - Clean, Deduplicate, Enrich, and Standardize data.

2. **Data Transformation & Verification**
    - Transform data to fit the Salesforce Schema.
    - Define External IDs for proper data mapping.

3. **Data Loading**
    - Group records by parents to avoid record locking during insertion.
    - Temporarily disable sharing settings.
        - Disable Flow, Trigger, and automation.
        - Enable defer sharing (to create cases in Salesforce).
    - Utilize Bulk API 2.0 for efficient parallel data loading.

4. **After Load**
    - Re-enable sharing settings.
        - Enable Flow, Trigger, and automation.
        - Disable defer sharing (to create cases in Salesforce).
        - Recalculate sharing settings.
    - Perform data integrity verification.

#### Diagram
![Data Migration](../../Images/CTA%20-%20Diagrams%20-%20Data%20Migration.png)
