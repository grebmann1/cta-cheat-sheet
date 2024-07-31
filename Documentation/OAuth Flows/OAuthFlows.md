[Table of Contents](../Documentation.md)

# OAuth Flows

## List of Flows

- Mobile & Browser
    - Web Server Flow
    - User Agent Flow
- Server
    - JWT Bearer Flow
    - SAML Bearer Flow
    - Client Credential Flow
    - Refresh Token Flow
    - Username and Password Flow
- IOT
    - Device Flow (Special)
    - Asset Token Flow (Special)

## SAML vs OpenId Connect

SAML is XML-based and is the most used SSO protocol. OpenID Connect is an extension of OAuth 2.0 with data structure in JSON. It's mainly used by social media applications.

## Terms & Definitions

### Authorization Code Request

The authorization code grant is used when an application exchanges an authorization code for an access token. After the user returns to the application via the redirect URL, the application will get the authorization code from the URL and use it to request an access token.

# SSO Flow

## SAML Flows

### IDP initiated Flow

In the IDP initiated Flow, we assume that the user is already logged in the IDP.

![IDP initiated](../../Images/CTA%20-%20Diagrams%20-%20SAML%20-%20IDP%20initiated.png)

### SP initiated Flow

![SP initiated](../../Images/CTA%20-%20Diagrams%20-%20SAML%20-%20SP%20initiated.png)

## OpenId Connect Flows

![OpenId Connect](../../Images/CTA%20-%20Diagrams%20-%20OpenId%20Connect.png)

# GENERAL OAUTH 2.0 FLOWS

## Mobile & Browser

### Web Server Flow

![Web Server Flow](../../Images/CTA%20-%20Diagrams%20-%20Web%20Server%20Flow.png)

### User Agent Flow

This is a deprecated flow. It's recommended to use the "Web Server Flow" with PKCE (Proof Key for Code Exchange)

![User Agent Flow](../../Images/CTA%20-%20Diagrams%20-%20User%20Agent%20Flow.png)

## Servers

### JWT Bearer Flow
JWT can include extra information such as user information, context, etc

![JWT Bearer Flow](../../Images/CTA%20-%20Diagrams%20-%20JWT%20Bearer%20Flow.png)

# Layered Flows (OAuth 2.0 with SAML or OpenId Connect)

### OAuth 2.0 User Agent with SAML

![User Agent with SAML](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20User%20Agent%20with%20SAML.png)

### OAuth 2.0 Web Server with SAML

![Web Server with SAML](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20Web%20Server%20with%20SAML.png)

### OAuth 2.0 User Agent with Social Sign On (OpenId Connect)

In this case, Salesforce represents the "Authorization Server" and the "Resource Server". It can be simplified that way to make it easier to understand.

![User Agent with Social Sign On](../../Images/CTA%20-%20Diagrams%20-%20OAuth%202.0%20User%20Agent%20with%20Social%20Sign%20On.png)
