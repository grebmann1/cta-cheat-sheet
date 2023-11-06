[Table of contents](../Documentation.md)
# Sharing

## What are the differents way of sharing records ?
- Organization-Wide Default
- Role Hierarchy
- Sharing Rules (Criteria & Ownership)
- Sharing Set (External User)
- Manual Sharing
- Apex Sharing
- Teams
- Territories

### Organization-Wide Default
Organization-Wide Default (OWD) estalish the sharing baseline for all standard and custom objects in the Salesforce instance.
The primary OWD includes :
- In general
    - Public Read/Write/Tranfer
    - Public Read/Write
    - Public Read-Only
    - Controlled by Parent
    - Private
- Case & Leads
    - Public Read/Write/Tranfer
    - Public Read/Write
    - Public Read-Only
    - Private 
- Campaign
    - Public Full Access
    - Public Read/Write
    - Public Read-Only
    - Private
- Pricebook
    - Use
    - View Only
    - No Access

`Accounts and Contracts are sharing the same OWD`.

#### Exception related to specific objects

- Knowledge sharing are controlled by "Data Categories" or "Standard Sharing"
- Product (No Sharing Rules except for Guest User)
- Person Account implies
    - Contact controlled by parents
    - Contact and Account Private


### Role Hierarchy
By default, 500 roles are allocated. This can be increased to 10k (Internal Roles)


### Teams
Teams are a particular sharing process specifically for a limited set of Salesforce standard objects including:
- `Account`
- `Opportunity`
- `Case`

