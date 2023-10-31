[Home](../../README.md)
# E-Signature

WARNING - Self made e-signature solution **aren't legit** !

## DocuSign
DocuSign is the leader in the market related to e-signature. 
1. [DocuSign Website](https://www.docusign.com/)
2. [DocuSign Documentation](https://developers.docusign.com/docs/salesforce/)

#### Features
 - E-Signature (Send via a email)
 - Slack integration
 - Documents are directly available in salesforce and can be tracked (records)
 - Apex toolkit to customize DocuSign
    - Envelope can be send via Flow, Trigger or Apex
    - Capture signature via code or iframe (for mobile app integration)

#### Integration
- **DocuSign Connect** is used to update "Status Object" from DocuSign to Salesforce
- Documents are signed in DocuSign Server
    - Rest API
    - Iframe or DocuSign site
- Custom Objects are used to represent the solution
    - DocuSign Status object 
    - DocuSign Recipient Status object

#### Similar tools
1. Adobe Acrobat Sign (Easy to integrate with Adobe pdf)
2. Conga Sign Sign (Work well with Conga composer)