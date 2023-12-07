[Table of Contents](../Documentation.md)

# Sharing

## Different Ways of Sharing Records
- Organization-Wide Default
- Role Hierarchy
- Sharing Rules (Criteria & Ownership)
- Sharing Set (External User)
- Manual Sharing
- Apex Sharing
- Teams
- Territories

### Organization-Wide Default
Organization-Wide Default (OWD) establishes the sharing baseline for all standard and custom objects in the Salesforce instance. The primary OWD includes:
- **In General**
    - Public Read/Write/Transfer
    - Public Read/Write
    - Public Read-Only
    - Controlled by Parent
    - Private
- **Case & Leads**
    - Public Read/Write/Transfer
    - Public Read/Write
    - Public Read-Only
    - Private
- **Campaign**
    - Public Full Access
    - Public Read/Write
    - Public Read-Only
    - Private
- **Pricebook**
    - Use
    - View Only
    - No Access

`Accounts and Contracts share the same OWD`.

#### Exceptions Related to Specific Objects

- Knowledge sharing is controlled by "Data Categories" or "Standard Sharing".
- Products (No Sharing Rules except for Guest User).
- Person Account implies:
    - Contact controlled by parents.
    - Contact and Account are Private.
- Account sharing rules and team sharing also provide control over:
    - `Account & Contract access`
    - `Case access`
    - `Opportunity access`

### Role Hierarchy
By default, 500 roles are allocated. This can be increased to 10k (Internal Roles).

### Teams
Teams are a particular sharing process specifically for a limited set of Salesforce standard objects, including:
- `Account`
- `Opportunity`
- `Case`

### Account Relationships and Account Relationship Data Sharing Rules
Account relationships and account relationship data sharing rules give you granular control over how account information is shared.\
They allow you to share object records related to an account, such as `cases`, `opportunities`, and `contacts`.\
The shared records don’t have to be owned by a user of that account, they just have to be associated with it.\ 
You can also determine the access level granted, such as read or write.

Use the object `Account Relationship` to provide granual to Partners accounts and use the 3 OTB fields:
- Account From
- Account To
- Account Relationship Type (Advertiser, Contractor, Broker, Client, etc)

