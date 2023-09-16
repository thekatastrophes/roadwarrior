# Security

[Home](../README.md) > [Solution Design](../README.md#solution-design) > Security ( [Previous](./3-architecture.md) / [Next](../4-decision-records/adr1-use-event-driven-serverless-microservice-architecture.md) )

We have considered the following security principles for our architecture:

* Authentication and Authorization: Only authorized users and services can access the microservices. (Token-based authentication and centralized identity providers.)
* Encryption: The data both in transit and at rest will be encrypted
* Message Security: Only trusted parties can publish and consume messages.
* The APIs will be exposed trough the API Gateway that provides additional layer of security.
* Rate Limiting and Throttling as a protection for DDoS attacks.
* Compliance: The system will take in consideration the compliance standards and regulations, such as GDPR, HIPAA, or PCI DSS and will implement the necessary controls and safeguards to meet compliance requirements, such as:
* Informing the users of the usage of cookies/storage
* Any personal information of the participant will be stored within the system with encryption and will be deleted once the legal deadline for storing personal information finishes.
* Participants can download their data in JSON format.
* Participants can request deletion of their data.
