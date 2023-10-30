# Experience Cloud

## External User Licenses
Important, it's forbidden to use `Experience Cloud Licenses` for internal users.

A user with a Partner Community license must be associated with a business account that is enabled as a partner account.\
`Partner users can’t be associated with person accounts`.

|License|Description|
|--|--|
| External App
| Customer Community
| Customer Community Plus
| Partner Community
| Channel

![Licenses](../../Images/ExperienceCloud_licence_1.png)

## Salesforce Features, Capability, and Custom Objects
|Feature| External App| Customer Community | Customer Community Plus | Partner Community | Channel |
|--|--|--|--|--|--|
| Accounts| Read & Edit| Read & Edit| ✅ | ✅ | ✅ |
| Contacts| ✅| ✅| ✅ | ✅ | ✅ |
| Cases|❌ | ✅| ✅ | ✅ |✅ |
| Knowledge | ✅| ✅| ✅ | ✅ | ✅ |
| Opportunities |❌|❌|❌| ✅ | ✅ |
| Leads|❌|❌|❌| ✅ | ✅ |
| Events|❌|Read Only|✅| ✅ | ✅ |
| Custom Objects*| 100| 10| 10| 10 | 10|
| Send Email| ❌|❌| ✅| ✅ | ✅ |
| Sharing Sets| ✅| ✅| ✅ | ✅ | ✅ |
| Advanced Sharing Rules |❌|❌| ✅| ✅ | ✅ |
| Reports & Dashboards |❌|❌| Read Only| ✅ | ✅ | ✅ |
| Territory Management|❌|❌|❌|✅|✅
| Workflow Approvals	|❌|✅|✅|✅|✅
| Extra Data Storage | 10MB | 0 | 2MB/1MB | 5MB/1MB | 5MB/1MB
| API Calls per Day | 200/400 | 0 | 200/10 | 200/10 | 200/10

[More details](https://help.salesforce.com/s/articleView?id=sf.users_license_types_communities.htm&type=5)
## Templates
Salesforce provide base template to quickly implement experience cloud such as :
- Help Center (Articles)
- Customer Service (Self service)
- Customer Account Portal
- Partner Central (Sales processes)

You can also create your own templates and use differents technologies such as :
- LWR (Lightning Web Runtime)
- Salesforce Tabs + Visualforce

## Experience Cloud Sites Usage Allocation
Experience Cloud site usage is governed by daily, monthly, and yearly allocations. Understanding these allocations is important to the success of your sites. `Add-on can be purchased`.

| EDITION | BANDWIDTH ALLOCATION (PER ROLLING 24-HOUR PERIOD PER COMMUNITY) | SERVICE REQUEST TIME (PER ROLLING 24-HOUR PERIOD PER SITE) | MAXIMUM PAGE VIEWS |
|--|--|--|---|
| Enterprise Edition  | 40 GB | 60h| 500k|
| Unlimited & Performance Edition   | 40 GB for production| 60 hours for production| 1M|

## Personal Contact Information visibility
Users can specify which information from their profile is visible to external users, such as customers and partners, and guests viewing publicly accessible pages that don’t require login.

When interacting with other Experience Cloud site members, it’s important to balance being visible and accessible with protecting your personal contact information. You may not want to show your job title, phone numbers, and other contact details outside of your internal organization. Your customers and partners may not want other customers and partners viewing all their contact information.

Use either the user interface or API to control visibility. You can choose to expose fields to employees only, members of the site from outside your company, or guest users who aren’t required to log in. Some fields are always visible to everyone accessing the site. Some fields allow up to three levels of visibility, while others allow fewer.

- `Employees` Only members from the internal organization can view.
- `External` Members from the internal organization and external members, such as customers and partners, can view. External users are those accessing Experience Cloud sites with community or legacy portal licenses.
- `Public` Anyone can view, including guest users viewing publicly accessible pages that don’t require login. Guest users can access public pages in sites via the Guest User license associated with each Experience Cloud site.


## Account Role Optimization (High Volumes Site)
If you expect a large volume of business accounts with a single Experience Cloud user, we recommend enabling Account Role Optimization (ARO) to ensure the best performance possible.\
If the account has a single user, then roles aren’t created for that account. Configure person account owner power users if your site must support even more customer or partner portal accounts.

ARO is really usefull to decrease the amount of external roles.

[More Informations](https://www.learnexperiencecloud.com/article/Configure-Account-Role-Optimization-to-Help-You-Scale-Your-Experience-Cloud-Users)

## External Roles 
|Role or Community User Allocations | Accocation | Details
|--|--|--|
|Total roles for users with licenses that require external users to be associated with roles.| `50k` |	This allocation includes all roles associated with users who hold licenses that require external users to be associated with roles, such as Customer Community Plus and Partner Community licenses. If you need more roles, **contact Salesforce Customer Support and ask for a Large User Volumes assessment.**|
|Maximum person account site users that a Salesforce user can own.| `50k` |**Contact Salesforce Customer Support to increase this allocation.**

As mentionned, the default allocation is `50k` roles but this can be increased with a SF case (Up to 500k with SF analysis and approval)