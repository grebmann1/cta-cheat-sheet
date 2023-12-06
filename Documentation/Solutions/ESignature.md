[Table of contents](../Documentation.md)

# E-Signature

**WARNING:** Self-made e-signature solutions **aren't legitimate**!

## DocuSign

DocuSign is a market leader in the e-signature domain, offering reliable e-signature services.

1. [DocuSign Website](https://www.docusign.com/)
2. [DocuSign Documentation](https://developers.docusign.com/docs/salesforce/)

### Key Features

- E-Signature facilitation via email
- Slack integration
- Direct availability of documents in Salesforce with tracking capabilities (records)
- Apex toolkit for DocuSign customization:
    - Sending envelopes via Flow, Trigger, or Apex
    - Signature capture via code or iframe (for mobile app integration)

### Integration

- **DocuSign Connect** updates the "Status Object" from DocuSign to Salesforce.
- Documents are signed in the DocuSign Server:
    - Using Rest API
    - Through an iframe or DocuSign site
- Custom Objects used in the solution include:
    - DocuSign Status object
    - DocuSign Recipient Status object

### Similar Tools

1. Adobe Acrobat Sign (Easily integrates with Adobe pdf)
2. Conga Sign (Works well with Conga Composer)
