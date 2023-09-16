# Event Broker

[Home](../README.md) > [Solution Design](../README.md#solution-design) > Event Broker ( [Previous](./4-microservices.md) / [Next](./6-data-storage.md) )

The Event Broker is a central component in event-based architecture responsible for receiving, managing, and routing events within a system. The application itself does not contain complex workloads that require orchestration, nor the services exchange messages so there is no need for a Message Bus or similar.