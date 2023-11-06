[Table of contents](../Documentation.md)
# Service Cloud  
## Features
### What features are included ?

- Service Console
- Knowledge Lightning
    - Einstein Article Recommendation
- Advanced Case Management
    - `Case email Auto response`
    - `Web & Email case capture`
    - Case auto assignement
    - `Case escalation rules & queues`
- Service contracts & entitlements
- `Omni-channel`
    - Skill Based, Queue Based and External routing.
    - Support Case, Lead and Work Order
- `Entitlement & Milestone`
- Next Best Action (AI empowered - 5k req/month)

### What features are available as an Add-On
- Live Agent (`Free with Unlimited edition`)
- Service Voice (CTI) [link](https://www.salesforce.com/products/service-cloud/solutions/call-center-management/?d=cta-body-promo-297)
- Einstein Bots (Chatbots)
- Live Messaging
- Feedback Management [link](https://www.salesforce.com/products/service-cloud/solutions/call-center-management/?d=cta-body-promo-297)
- Field Service
- Appointment Assistant
- Sales & Service Cloud bundle


# Documentation 

## Important Products/ Add - on
|Product|Description| Unlimited | Unlimited + |
|--|--|--|--|
|Knowledge|Self explenatory|✅ |✅ 
|Sandbox|Self explenatory|✅ |✅ 
|Feedback Management|Improve customer experiences by capturing contextual feedback to deliver superior service [link](https://www.salesforce.com/editions-pricing/platform/feedback-management/)|$ |✅ 
|Service Cloud Voice|Connect with customers with call centre integration built directly into your CRM. Provide personalised service in every phone call with easy-to-use Service Cloud Voice. Real-time call transcription (with Amazon) [link](https://www.salesforce.com/eu/products/call-center-integration/)|$ |✅ 
|Digital Engagement| Reach customers across every digital channel — including mobile messaging, web chat, and more — to provide a seamless service experience all on the #1 platform for service. (Messenger, Whatsapp, SMS and Chatbot) `1k SMS included` [link](https://www.salesforce.com/editions-pricing/service-cloud/digital-engagement/) |$ |✅ 

## Data Model
### Overview
![Data Model](/Images/CTA%20-%20Diagrams%20-%20Service%20Cloud.png)

## Routing
### Omnichannel

Omni-Channel is a flexible, customizable feature, and you can configure it declaratively—that is, without writing code. Use Omni-Channel to manage the priority of work items, which makes it a cinch to route important work items to agents quickly.\
Manage your agents’ capacity to take on work items so that they’re given only the number of assignments that they can handle. You can also define which agents can work on different types of assignments. For example, you can create one group of agents to respond to leads and sales inquiries, and another group that helps customers with support questions.

Omni-Channel routes work requests to the most available and qualified support agents in the console. You can also provide real-time operational intelligence to support supervisors with Omni Supervisor. Agents no longer have to pick and choose work assignments manually from a queue, which saves everyone in your call center time, effort, and brainpower. Because it’s easier for agents to work on their assignments, they can assist your customers faster and more effectively and close assignments more quickly.

Routing logic is applied when work is assigned to an owner. If field values on the work item are changed after the item is routed, the routing logic isn’t reapplied.

### Assignement Rules
Assignment rules automate your organization’s lead generation and support processes.\
Use lead assignment rules to specify how leads are assigned to users or queues. Use case assignment rules to determine how cases are assigned to users or put into queues.

### Auto-Response Rules
Create auto-response rules for leads captured through a Web-to-Lead form and for cases submitted through a:
- Self-Service portal
- Customer Portal
- Web-to-Case form
- Email-to-Case message
- On-Demand Email-to-Case message

Case auto-response rules are also available in the Essentials edition.

Create as many response rules as you like based on any attribute of the incoming lead or case. Keep in mind that you can activate only one rule for leads and one rule for cases at a time. Your team can see the email responses in the Activity History related list for the lead or contact and in the Email related list on cases.

Emails sent from case auto-response rules don’t count towards the daily limit for outbound email messages.

### Entitlement & Milestones
![Entitlement & Milestones](../../Images/CTA%20-%20Diagram%20-%20Service%20Cloud%20-%20Entitlement.png)

Case Milestones can be auto-completed with a trigger record flow that close the CaseMilestone based on specific criterias.

### Escalation Rules
Escalation rules automatically escalate cases when the case meets the criteria defined in the rule entry.\
You can create rule entries, which define criteria for escalating a case, and escalation actions, which define what happens when a case escalates.


### Limits for Assignment, Auto-Response, and Escalation Rules
Salesforce limits the number of rules, as well as the number of entries and actions per rule. These limits apply to assignment rules, auto-response rules, and escalation rules.

| LIMIT                                   | VALUE  |
|-----------------------------------------|--------|
| Total rules across objects              | 2k     |
| Active rules per object                 | 50     |
| Total rules per object                  | 500    |
| Entries per rule                        | 3k     |
| Formula criteria entries per rule       | 300    |
| Filter criteria per rule entry          | 25     |
| Actions allowed per rule                | 200    |
