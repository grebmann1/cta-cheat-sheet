[Home](../../README.md)
# Security - Compliance

## PCI 
PCI stand for `Payment Card Industry`.
It's an industry standard that need to be followed.

These informations **need** to be encrypted:
- Card Holder Information
- Card Number
- Card Expiration Date

These information **can't** be stored.
- Pin (Even encrypted)
- CVV/CVC
- Authentication Data

### Is Salesforce PCI compliant ?
Salesforce is PCI compliant if you use the `Salesforce Billing package` as salesforce doesn't store any credit card information from the user and use a token to communicate with the payment gateway.

Each payment record contain these information:
- Name on card
- Last four digits of credit card number
- Card Type
- Token
- Expiration month and year

In case you want to store it using `Salesforce Standard`, then you should only store the `Token` provided by the payment gateway. Storing only the payment token is compliant !


## PHI - HIPAA
PHI stand for `Protected Health Information`