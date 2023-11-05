# Common Pattern

The goal of this section is to group the most common pattern to apply to your solution when a specific requirement is coming out.


## Assumption to take

- Budget is not a constraint.
- Buy over build is recommended.
- REST API available if not specified/mentionned.
- Systems have "on change" capabilities to execute code and/or send event

## Support multiple languages
Key feature to mention:
- Translation Workbench
- Custom Labels
- VF Email templates
- OOTB language selector component for Experience Cloud

## Support multiple currencies
 Enable multi currencies


## Data need to be migrated
For data migration, you should consider this flow : 

1. Data Extraction & Data Cleaning
    - Connect the system to your ETL
    - Clean, Deduplicate, Enrich and Standardize
2. Data Transformation & Verifications
    - Transform to Salesforce Schema
    - Define External ids
3. Data Loading
    - Group record by parents (Avoid record locking)
    - Disable sharings
        - Disable Flow, Trigger and automation.
        - Enable defer sharing (Case to salesforce need to be created).
    - Load data in parallel with Bulk Api 2.0
4. After load
    - Enable sharings
        - Enable Flow, Trigger and automation.
        - Disable defer sharing (Case to salesforce need to be created).
        - Recalculate sharing
    - Verify the data integrity

#### Diagram
![Data Migration](../../Images/CTA%20-%20Diagrams%20-%20Data%20Migration.png)
