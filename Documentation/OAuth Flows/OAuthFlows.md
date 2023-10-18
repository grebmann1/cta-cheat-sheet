# OAuth Flows

## List of Flows

- Web Server Flow
- User Agent Flow
- JWT Bearer Flow
- Device Flow (Special)
- Asset Token Flow (Special)
- Username and Password Flow
- Refresh Token Flow
- SAML Assertion Flow
- SAML Bearer Assertion Flow (Similar to Refresh but use SAML)

## SAML vs OpenId Connect
SAML is xml based and is the most used SSO protocol.
OpenId Connect is an extension of OAuth2.0 with data structure in JSON. (Mainly used by social media application.)


# SSO Flow
## SAML Flows
### IDP initiated Flow
In IDP initiated Flow, we assume that the user is already logged in the IDP.

![IDP initiated](../../Images/CTA%20-%20Diagrams%20-%20SAML%20-%20IDP%20initiated.png)
### SP initiated Flow
![SP initiated](../../Images/CTA%20-%20Diagrams%20-%20SAML%20-%20SP%20initiated.png)

## OpenId Connect Flows
![OpenId Connect](../../Images/CTA%20-%20Diagrams%20-%20OpenId%20Connect.png)

# GENERAL OAUTH 2.0 FLOWS
## Web Server Flow
![Web Server Flow](../../Images/CTA%20-%20Diagrams%20-%20Web%20Server%20Flow.png)
## User Agent Flow
![User Agent Flow](../../Images/CTA%20-%20Diagrams%20-%20User%20Agent%20Flow.png)
## JWT Bearer Flow
![JWT Bearer Flow](../../Images/CTA%20-%20Diagrams%20-%20JWT%20Bearer%20Flow.png)


# Layered Flows (OAuth 2.0 with SAML or OpenId Connect)

### OAuth 2.0 User Agent with SAML
![User Agent with SAML](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20User%20Agent%20with%20SAML.png)

### OAuth 2.0 Web Server with SAML
![Web Server with SAML](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20Web%20Server%20with%20SAML.png)

### OAuth 2.0 User Agent with Social Sign On (OpenId Connect)

In this case, Salesforce represent the "Authorisation Server" and the "Resource Server". It can be simplified that way to make it easier to understend.

![User Agent with Social Sign On](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20User%20Agent%20with%20Social%20Sign%20On.png)