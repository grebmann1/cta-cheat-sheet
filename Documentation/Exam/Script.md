[Table of Contents](../Documentation.md)
# Scripts 
As a Salesforce Certified Technical Architect (CTA), your ability to present your solution effectively is just as important as designing it. 

A well-prepared script is crucial for guiding your responses during the CTA review board.\
This script will help ensure you address key sections **comprehensively**, **stay focused**, and communicate your decisions **confidently**.

# Sections
## Overview
#### General
- XXX is an XXX company and provides XXX Services to XXX
- They are operating in XXX regions/countries.
- Goal of this project is to XXXX
- I would like to highlight potential risks and propose corresponding mitigation strategies:
    - XXX
    - XXX
- I recommend to Enable **Multi Language** to provide translations using the different mechanism:
    - Translation Workbench
    - Custom Label
    - Language Picker for Experience Cloud
- I recommend to Enable **Multi Currency** and to set the org currency to ___

#### Org Strategy
- I recommend to use **Single** Org Strategy because of 
    - **Standardized Business Process** (Add governance if needed)
    - **No Data Residency** Requirement
    - No performance Issues enforcing multi org

OR

- I recommend to use **Multi** Org Strategy because of 
    - **Different Business process** | **regional complexity** | **Sharing complexity** that will make it complex to maintain the application and also impact the time to market
    - **Regional regulations** that mandates to go for separate orgs

#### Assumptions
- I took a few assumptions:
    - REST API available by default if not mentioned.
    - Budget isn't a constrain but should be used wisely.
    - IOT can be purchased pre-setup.

## Persona
Let’s have a look in to the Actor and their Licenses\
(Repeat for Every User, Group users to make it fast)

XXX is an Internal User, I propose to use XXX license since access to XXX  is needed

- `List the Feature licenses under users.` 
- `List the Add on licenses.` 
- `List any user that is there in the scenario but not given any license.` 

### Role Hierarchy
Let's check the Role hierarchy for XXX.  

The roles are split by (Region|Function), The regional XXX reports to CEO.\
`Take one of the branches and explain all the hierarchy and conclude with`  
Likewise other regions have similar structure.  

### System Landscape
Let's check the System Landscape

`Explain the legend`
Let's review the how the users access Salesforce first ?
- Internal Users
- Customers
- Partners/Agents

Related to mobile app, I'm recommending:

... **Mobile Publisher** for branded mobile apps and no requirements for pixel perfect user interface or advance offline capabilities.

OR

... **Standard App** since there is no requirements for pixel perfect user interface or advance offline capabilities. (Internal Only).

OR

... **Hybrid App** for perfect UI, Offline, etc ...

For **Build vs Buy** decision, i am proposing XXX solution. This give us operation gain and save time to market.

In term of document strategy:
`Do the calculation and highlight it`

I propose to use SF files to store the files. Storage can be purchased as an Add-on.

OR

I propose to use SDrive or XXX to store the files as we need to have large files and/or need to store the files in specific countries.

### Data Model

### Large Data Volume

### Busines Requirements

### Development Lifecycle & Governance
Let's review the testing strategy and environment type.

My recommended environments setup is based on storage capacity and refresh cycle.\
`Propose a solution based on the scenario `
- Development (Scratch Org, 200mb) 
- Merge (Scratch Org 200mb)
- QA (Dev Pro 1GB)
- UAT (Partial 5GB)
- Stage (Full Sdbx)
- Prod

I recommend source-driven development where XXX is the source control system comprising the code base. 
Developers would implement the features in scratch orgs, unit test the feature and raise a pull request in XXX.

To improve the quality, I recommend to:
- use **SFDX Code Analyser** to do static code analysis.
- use **Selenium** to automatise UI testing.