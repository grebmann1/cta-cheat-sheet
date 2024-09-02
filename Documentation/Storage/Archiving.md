[Table of Contents](../Documentation.md)

# Archiving

## Different Archiving Strategies

When archiving, decide whether to store data in Salesforce `Big Objects` or externally in a Data Warehouse or Data Lake. Avoid using Big Objects for the CTA exam due to justification difficulties and potential issues with Salesforce Shield.

### Recommended External Solutions:
- **Data Lake:** `Amazon S3 Bucket` (Data & Files)
- **Data Warehouse:** `Snowflake` (Data & Files)

## Archive LDV Records

Archiving Large Data Volumes (LDV) is crucial to maintain optimal performance in your Salesforce org.

## Salesforce Solutions

No specific Salesforce product exists for archiving, but AppExchange offers solutions to archive data in Big Objects and make them accessible via LWC components.

## External Solutions

### Own - Data Archive

`Own - Data Archive` is ideal for managing archiving schedules and storing data in Amazon S3. It also provides data virtualization via a library of Lightning components.

![Salesforce Backup](../../Images/ownbackup-1.png)

## Recommendation for CTA Exam

While `Own Data Archive` offers comprehensive capabilities, it involves migrating all data into Salesforce before archiving, which is difficult to defend in the CTA exam. The preferred pattern involves archiving data during the migration process, providing access via OData, and having a scheduled archiving plan.

### Recommended Solutions:

#### 1. **PostgreSQL on Heroku**
- **Components:**
  - Heroku Connect (External Object)
  - REST API (LWC)
  - Files not supported (Consider using an S3 Bucket)
  - Provides a connector for CRM Analytics
- **Pros:**
  - Seamless integration with Salesforce
  - Real-time data synchronization
  - Suitable for structured data

#### 2. **AWS S3 Bucket**
- **Components:**
  - Middleware with OData Connector (External Objects)
  - REST API (LWC)
  - File supported
  - Provides a connector for CRM Analytics
- **Pros:**
  - Scalable and cost-effective
  - Supports structured and unstructured data
  - Easy integration with AWS services

#### 3. **Snowflake (Using AWS S3)**
- **Components:**
  - Middleware with OData Connector (External Objects)
  - REST API (LWC)
  - File supported
  - Provides a connector for CRM Analytics
- **Pros:**
  - High-performance data warehousing
  - Scalable and flexible
  - Extensive data analytics capabilities

These solutions leverage ETL processes and are easier to defend in the CTA exam, aligning with best practices expected by the judges. Each option offers a robust and scalable approach to data archiving while ensuring seamless access and integration with Salesforce.

# Backup Solution

## Salesforce Solution - Salesforce Backup

`Salesforce Backup` manages backups directly from Salesforce, storing data in AWS via the `Bulk API (Web Server flow)`. However, it only supports daily backups and does not yet support files (as of November 2023), making it less suitable for enterprise needs.

![Salesforce Backup](../../Images/CTA%20-%20Diagrams%20-%20Salesforce%20Backup.png)

## External Solution

`Own - Backup` is ideal for managing backup schedules and storing data in Amazon S3.

## Custom Built Solution

Consider custom-built solutions tailored to specific backup and archiving needs.
