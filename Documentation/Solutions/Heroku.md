[Table of Contents](../Documentation.md)

# Heroku

Heroku is a platform as a service (PaaS) that empowers developers to build, run, and manage applications entirely in the cloud.

Heroku is highly scalable and offers specific features facilitating the integration of external applications with Salesforce, along with addressing various compliance issues.

## Heroku Shield

Heroku Shield is an additional package available to Heroku Enterprise customers. `Apps operating under Shield run within a network-isolated Heroku Shield Private Space`, utilizing Heroku Shield Private Dynos to enhance runtime security.

### Compliance Regulations Supported

1. PHI - HIPAA (Protected Health Information)
2. PCI - Level 1 (Payment Card Industry)
   - Secure storage of payment tokens

### Heroku Shield Postgres

Shield Postgres extends Heroku Postgres, ensuring encryption of sensitive data in transit and at rest.

### Kafka on Heroku Shield

Apache Kafka on Heroku Shield combines the leading open-source solution for managing event streams with strict controls to deliver real-time, HIPAA-compliant applications.

## Heroku Connect

Heroku Connect is an add-on that synchronizes data between a Salesforce organization and a Heroku Postgres database.
By utilizing Heroku Connect with Heroku Postgres, custom applications can interact seamlessly with Salesforce data.

**Note:** `A license for each integration user is required`. Heroku Connect can leverage 'Shield' for compliance purposes.
