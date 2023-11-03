[Table of contents](../Documentation.md)
# CTI Solutions
When you want to integrate a telephony system with Salesforce you need to use a CTI solution.
There is multiple CTI solution available in App Exchange but they are mainly specific to certain telephony providers.

The best practice is to first look for a solution matching your telephony system in App Exchange before building something custom with Open CTI.

## Salesforce Terminologies
| Term | Description|
|--|--|
| Softphone| An on-screen phone for making and receiving calls.|
| Call Center| A Salesforce feature that integrates with call systems developed by partners or developers.|
| Open CTI| A JavaScript API for building cloud-based call systems to be used with Salesforce's Call Center. Open CTI is browser and platform agnostic, allowing support agents to make calls on a variety of browsers and platforms, such as Microsoft Internet Explorer, Mozilla Firefox, Apple Safari, or Google Chrome on Mac, Linux, or Windows, providing flexibility and choice for support agents.|



![Open CTI](../../Images/CTI-1.png)


1. [Open CTI Documentation](https://developer.salesforce.com/docs/atlas.en-us.api_cti.meta/api_cti/sforce_api_cti_intro.htm)

## Key Features of OPEN CTI
- Receive Call
- Make Call
- Search and pop records in softphone layout
- Save Salesforce records
- Execute Apex

## Integration
 - Javascript Library 
    - Visualforce or any other web technology (LWC not supported yet except for click-to-dial for making a call)
 - Lightning message
 
### Softphone
A softphone is a customizable call-control tool that appears to users assigned to a call center. A softphone's functionality and user interface are determined by the Salesforce admin.
Softphone is integrated in Salesforce via an IFrame. The softphone is provided by the Telephony system and configured in Salesforce under : **Call Centers**



## Licenses
1. Open CTI (Available without Extra)
2. Sales Dialer (Sales & Service cloud with an **Extra Add-on license**)
    - ❌ Only work to the US and Canada ❌

## List of Solutions (Sample)
This is a non exhaustive list of solutions availables in App Exchange

1. **AirCall CTI** (To Recommend if there is no specific telephony System)
    - Web softphone (available on mobile via an App)
    - Monitor and listen to agents (live) and  measure KPIs
    - Connect to other system (Help Desk, etc)
    - Send SMS
    - [App Exchange Link](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3A00000EFnzwUAD)


## Documentation

1. [Trailhead](https://trailhead.salesforce.com/content/learn/modules/service_call)