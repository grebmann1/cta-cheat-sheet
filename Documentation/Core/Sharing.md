[Table of Contents](../Documentation.md)

# Sharing

## Overview of Sharing Methods in Salesforce
Salesforce provides multiple ways to manage and control record sharing. These methods ensure that the right users have the right access levels. Here are the primary methods of sharing:

- Organization-Wide Default (OWD)
- Implicit Sharing (Parent-Child Relationships)
- Role Hierarchy
- Sharing Rules (Ownership-Based and Criteria-Based)
- Sharing Sets (for External Users)
- Manual Sharing
- Apex Sharing
- Teams
- Territory Management

### Organization-Wide Default (OWD)
OWD establishes the baseline sharing settings for both standard and custom objects across your Salesforce instance. These settings define the default access levels for records users don’t own. The primary options include:

#### General Sharing Options
- **Public Read/Write/Transfer**
- **Public Read/Write**
- **Public Read-Only**
- **Controlled by Parent**
- **Private**

#### Case & Lead Specific Sharing Options
- **Public Read/Write/Transfer**
- **Public Read/Write**
- **Public Read-Only**
- **Private**

#### Campaign Sharing Options
- **Public Full Access**
- **Public Read/Write**
- **Public Read-Only**
- **Private**

#### Pricebook Sharing Options
- **Use**
- **View Only**
- **No Access**

**Note**: *Accounts and Contracts share the same OWD settings.*

#### Object-Specific Sharing Exceptions

##### General
- **Knowledge**: Sharing is controlled through *Data Categories* or *Standard Sharing*.
- **Products**: No sharing rules, except for Guest Users.
- **Person Accounts**: 
    - Contact is controlled by the parent account.
    - Both Contact and Account default to Private sharing.
- **Account Sharing Rules & Team Sharing**: Control access to associated objects like:
    - `Account & Contract`
    - `Case`
    - `Opportunity`

##### Experience Cloud
Using **Contacts with Multiple Accounts**, you can grant access to records via contact relationships with different accounts using sharing sets. For example:
- Use `Contact.RelatedAccount` to access records associated with different accounts instead of just the primary account.

### Role Hierarchy
Salesforce allocates 500 internal roles by default, with the option to increase this limit to 10,000. Roles allow users higher up the hierarchy to inherit the sharing settings of users below them.

### Teams
Teams provide a specialized sharing mechanism for key Salesforce standard objects, allowing users to collaborate on:
- `Accounts`
- `Opportunities`
- `Cases`

### Account Relationships and Data Sharing Rules
Account relationships and related data sharing rules offer granular control over how account-related data is shared. This method allows you to share object records related to an account (such as `Cases`, `Opportunities`, and `Contacts`) without requiring the records to be owned by a user of that account. You can set varying access levels, such as *Read* or *Write*.

Use the `Account Relationship` object to share data between accounts and partners, leveraging the following fields:
- **Account From**
- **Account To**
- **Account Relationship Type** (e.g., Advertiser, Contractor, Broker, Client)

[Official Documentation](https://help.salesforce.com/s/articleView?id=sf.networks_partner_account_relationships_and_sharing.htm&type=5)

## Sharing Limits in Salesforce

Salesforce imposes limits on the number of sharing rules per object to ensure system performance. These limits are as follows:

1. **General Sharing Rules Limit**: This applies to all sharing rules, including both ownership and criteria-based rules. The default limit is 300, but it can be increased to 500 through a support case.
2. **Criteria-Based Sharing Rules Limit**: Salesforce allows up to 50 criteria-based sharing rules by default, but this limit can be increased to 200 via a support case.

| Type of Sharing Rule            | Limit | Comments |
|----------------------------------|-------|----------|
| Sharing Rules (Ownership & Criteria-Based) | 300   | Can be increased to 1,000 via support. |
| Criteria-Based Sharing Rules     | 50    | Can be increased to 200 via support.    |
| Restriction Rules                | 5 per object | Restricts records available to users. Applies to custom objects, external objects, contracts, events, tasks, and more. |

**Note**: *Excessive sharing rules may impact performance, particularly during record inserts and updates. It is advisable to regularly review sharing rules and optimize them as necessary.*
