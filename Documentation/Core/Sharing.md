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

- Knowledge sharing is controlled by "Data Categories" or "Standard Sharing."
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
