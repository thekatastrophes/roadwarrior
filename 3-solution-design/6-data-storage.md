# Data Storage

[Home](../README.md) > [Solution Design](../README.md#solution-design) > Data Storage ( [Previous](./5-event-broker.md) / [Next](./7-front-end-technology.md) )

Each microservice has its own database, ensuring data isolation as well as maintain the bounded context, preserve the autonomy (changes of the data models and schemes do not affect other microservices), each microservice can scale separately, and if needed each microservice can have different database type (relational, noSQL or other).
