[Table of Contents](../Documentation.md)

# Common Pattern

This section outlines common patterns and best practices to address specific requirements in Salesforce solutions.

## Assumptions

- Financial resources are not a constraint.
- Opting for pre-built solutions over custom development is recommended.
- Availability of REST APIs if not otherwise specified.
- Systems support triggering events on data changes.

## Multilingual Support

Implementing multilingual support involves several key considerations:
- Leveraging the Translation Workbench for translating UI labels and error messages.
- Using Custom Labels for translating text that appears in the UI, such as button labels, field names, and picklist values.
- Using Visualforce (VF) Email templates that support multiple languages for consistent communication.
- Utilizing the out-of-the-box language selector component available in Experience Cloud.

## Multiple Currencies Support

Enabling multi-currency support within Salesforce for managing deals, opportunities, and transactions across different currencies.

## Data Migration Strategies

Refer to the [Data Migration](DataMigration.md) page for methodologies and approaches, such as:
- Big Bang: A one-time data migration approach.
- Trickle Migration: An incremental migration method that works in iterations.

## Specific Scenarios:

### Requirement 1: Data Retention Policy

Scenario:
- Customers require access to orders from the last 2 years, while support agents need access to the last 5 years.

Considerations:
- Long Data Visibility (LDV) settings.
- Archiving solutions or processes.

Solutions:
1. Archive older data while providing a Lightning Web Component (LWC) for data visualization.
2. Adjust sharing settings selectively to manage data access based on roles.

### Requirement 2: Controlled Field Editability

Scenario:
- The order amount should only be editable by the "Sales Manager" and their superior once the order status is Confirmed.

Considerations:
- Implement Field-Level Security (FLS) for restricting access to the field.
- Validate logic or conditions before allowing edits.

Solutions:
- Utilize Validation Rules or Apex Triggers to enforce field edit restrictions.
- Evaluate the potential use of Dynamic Forms (if applicable).

### Requirement 3: Single Org for Multiple Regions

Scenario:
- Operating with a single org/region, requiring Experience Cloud usage and centralized user management.

Solution:
- Utilize Experience Cloud for external access and engagement.
- Establish a centralized user management system within Salesforce.

### Requirement 4: Reporting Over Multiple Regional Data in a Single CRM Analytics Instance

Scenario:
- Need to aggregate data from multiple regional sources for consolidated reporting within a single CRM Analytics instance.

Solutions:
- Implement anonymization techniques to avoid sending Personally Identifiable Information (PII).
- Consider utilizing Data Virtualization techniques to create a unified view of the data.

### Requirement 5: Complex Discount and Price Variations

Scenario:
- Handling multiple levels of discounts with different price variations within orders.

Solutions:
- Evaluate and utilize solutions provided by Salesforce to accommodate complex pricing structures.
- Avoid overcomplicating the process with unnecessary customizations.

### Requirement 6: Handling Large Data Volume

Scenario:
- Managing 1 million orders and 1 million assets annually, encountering performance challenges.

Considerations:
- Large Data Volume (LDV) considerations.
- Archiving solutions for reducing data volume and improving system performance.

Solutions:
- Implement strategies to optimize Large Data Volume (LDV) handling within Salesforce.
- Consider archiving solutions for managing historical data effectively.

### Notes

- Use Leads specifically for managing "Potential" entities and avoid repurposing the Case object for this scenario.
- Review and fine-tune Account Relationship Sharing rules and Manager Group Sharing for optimal data access control.
- Consider Privacy Center functionality for archiving and maintaining clean data records, including archiving fields, leveraging Record Type (RT)-based Sharing, and reviewing consent forms.

These guidelines are aimed at optimizing data management practices, sharing rules, and object utilization within Salesforce, ensuring efficient and effective business operations.
