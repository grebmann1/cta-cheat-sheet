# Experience Cloud

## External User Licenses

It's forbidden to use Experience Cloud Licenses for internal users. Different licenses and their descriptions include:

| License | Description |
|---------|-------------|
| External App |
| Customer Community |
| Customer Community Plus |
| Partner Community |
| Channel |

![Licenses](../../Images/ExperienceCloud_licence_1.png)

## Salesforce Features, Capability, and Custom Objects

A comparison of features across different community licenses:

| Feature | Customer Community | Customer Community Plus | Partner Community | External App |
|---------|--------------------|-------------------------|-------------------|--------------|
| Accounts|  Read & Edit| ✅ | ✅ |Read & Edit|
| Contacts|  ✅| ✅ | ✅ | ✅|
| Assets|  ✅| ✅ | ✅ | ✅|
| Contracts | ✅| ✅ | ✅ |  ✅|
| Cases| ✅| ✅ | ✅ |❌ |
| Knowledge | ✅| ✅ | ✅ |  ✅|
| Order | ✅| ✅ | ✅ |  ✅|
| Product| Read Only| Read Only | Read Only | Read Only|
| Pricebook| Read Only| Read Only| Read Only| Read Only | 
| Opportunities |❌|❌| ✅  |❌
| Leads|❌|❌| ✅ | ❌|
| Tasks| Read Only | ✅ | ✅| ✅ |
| Calendar & Events|Read Only|✅| ✅ | ✅|
| Service Contract|  ❌| ✅ | ✅ | ✅|
| Work Order| ✅| ✅ | ✅ | ✅|
| Custom Objects| 10| 10| 10 | 100|
| Send Email| ❌| ✅| ✅ |❌|
| Sharing Sets| ✅| ✅ | ✅ | ✅|
| Account Teams |❌| ❌| ✅ | ❌|
| Advanced Sharing Rules |❌|❌| ✅ |  ✅|
| Omnichannel |❌|❌| ❌| ❌| ❌ |
| Reports & Dashboards |❌| Read Only| ✅ | ✅ | ❌|
| Territory Management|❌|❌|✅|✅|
| Workflow Approvals|✅|✅|✅|❌|
| Extra Data Storage | 0 | 2MB/1MB | 5MB/1MB | 10MB |
| Extra File Storage | 0 | 2MB/1MB | 5MB/1MB | 10MB |
| API Calls per Day |  0 | 200/10 | 200/10 | 200/400 |

[More details](https://help.salesforce.com/s/articleView?id=sf.users_license_types_communities.htm&type=5)

## Templates

Salesforce provides base templates for Experience Cloud, including Help Center (Articles), Customer Service (Self-service), Customer Account Portal, and Partner Central (Sales processes). Users can also create custom templates using technologies like LWR (Lightning Web Runtime) and Salesforce Tabs + Visualforce.

## Experience Cloud Sites Usage Allocation

Usage of Experience Cloud sites is regulated by daily, monthly, and yearly allocations. Add-ons can be purchased for extended usage. Allocations differ across editions.

| EDITION | BANDWIDTH ALLOCATION (PER ROLLING 24-HOUR PERIOD PER COMMUNITY) | SERVICE REQUEST TIME (PER ROLLING 24-HOUR PERIOD PER SITE) | MAXIMUM PAGE VIEWS |
|--|--|--|---|
| Enterprise Edition  | 40 GB | 60h| 500k|
| Unlimited & Performance Edition   | 40 GB for production| 60 hours for production| 1M|

## Personal Contact Information Visibility

Users can control the visibility of their personal contact information based on categories like "Employees," "External," and "Public." This control can be exercised via the UI or API.

## Account Role Optimization (High Volume Site)

For high-volume sites, Account Role Optimization (ARO) helps optimize performance by reducing external roles, especially with a large volume of business accounts having a single Experience Cloud user.

[More Information](https://www.learnexperiencecloud.com/article/Configure-Account-Role-Optimization-to-Help-You-Scale-Your-Experience-Cloud-Users)

## External Roles 

Information about external roles and allocations:

| Role or Community User Allocations | Allocation | Details |
|------------------------------------|------------|---------|
| Total roles for users with licenses that require external users to be associated with roles | 50k | This allocation includes all roles associated with users who hold licenses requiring external users to be associated with roles, such as Customer Community Plus and Partner Community licenses. For more roles, contact Salesforce Customer Support. |
| Maximum person account site users that a Salesforce user can own | 50k | Contact Salesforce Customer Support to increase this allocation. |

The default allocation for roles is 50k but can be increased with a Salesforce case (up to 500k with analysis and approval).
