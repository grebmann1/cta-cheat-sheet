[Table of Contents](../Documentation.md)

# Salesforce Subscription Management
# Salesforce Subscription Management

## Overview

Salesforce Subscription Management is an add-on product designed to streamline subscription-based business models within the Salesforce ecosystem. It offers robust tools and functionalities to `manage subscription lifecycles, billing, revenue recognition, and customer engagement` seamlessly.

### Key Features

- **Subscription Lifecycle Management**: Easily create, modify, and cancel subscriptions with automated processes for renewals and upgrades/downgrades.
- **Flexible Billing Solutions**: Configure and customize billing schedules, pricing tiers, and invoicing based on subscription terms and conditions.
- **Revenue Recognition Automation**: Automate revenue recognition processes compliant with accounting standards (e.g., ASC 606/IFRS 15) for accurate financial reporting.
- **Customer Self-Service Portal**: Empower customers to manage their subscriptions, view invoices, update payment methods, and access support through a self-service portal.
- **Analytics and Reporting**: Gain insights into subscription performance, churn rates, revenue forecasts, and customer behavior through intuitive dashboards and reports.

## Use Cases

### 1. Subscription-Based Businesses

`Suitable for companies operating on subscription-based models such as Software as a Service (SaaS), media streaming, membership services, and more.` Manage recurring revenue streams efficiently and adapt subscription offerings to evolving customer needs.

### 2. Financial Compliance

Assist finance teams in adhering to revenue recognition standards by automating revenue schedules and ensuring compliance with accounting regulations like ASC 606 and IFRS 15.

### 3. Enhanced Customer Experience

Empower customers with self-service capabilities to manage their subscriptions, leading to higher satisfaction levels and reduced support inquiries.

## Licenses

The licensing model is based on permission set licenses. When a permission set is assigned to the user, the permission set license is consumed.
- Subscription Management Experience Cloud User
- Subscription Management Partner User
- Subscription Management User



### Objects Used and Created

The Salesforce Subscription Management add-on utilizes various Salesforce standard and custom objects to manage subscriptions, billing, and related data. Below is a table representing some key objects:

| Object Name | Purpose |
|-------------|---------|
| Subscription| Represents a customer's subscription to a product/service.    |
| Subscription Product| Defines the products/services included in a subscription.|
| Billing Contract| Manages the billing terms and conditions for subscriptions.   |
| Revenue Schedule| Handles revenue recognition schedules based on subscriptions. |
| Subscription Invoice| Generates invoices for subscription charges and fees.|
| Self-Service Portal| Provides customers access to manage their subscriptions.|
| Analytics Dashboard| Offers insights into subscription performance and metrics.|

## Data Model

### Product
![Data Model](../../Images/CTA%20-%20Diagrams%20-%20Subscription%20Management%20-%20Product.png)

### Order
![Data Model](../../Images/CTA%20-%20Diagrams%20-%20Subscription%20Management%20-%20Order.png)

## Links
- [Subscription Management Developer Guide](https://developer.salesforce.com/docs/revenue/subscription-management/guide/introduction.html)