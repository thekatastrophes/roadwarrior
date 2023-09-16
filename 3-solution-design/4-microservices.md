# Microservices

[Home](../README.md) > [Solution Design](../README.md#solution-design) > Microservices ( [Previous](./3-architecture.md) / [Next](./5-event-broker.md) )

Considering the architectural aspects, we previously discussed—scalability, interoperability, availability, and feasibility—we propose the use of serverless microservices as described in [ADR1](../4-decision-records/adr1-use-event-driven-serverless-microservice-architecture.md).

The following criteria was used to determine when a certain piece of functionality is to be considered a Microservice:

* The functionality must scale or be deployed independently from other parts.
* The functionality should have a clear and well-defined purpose or responsibility.
* The functionality can be written in a separate language/technology based on pragmatic considerations such as the expertise of the development team or the specific requirements of the service.
* The functionality must be isolated by a clean boundary.

Given the above principles, the following are identified as Microservices:

* User Profile
* E-Mail Integrator
* Trip Coordinator
* Reservation Coordinator
* Travel System Integrator
* Notification Sender
* Analytics Service
* Report Generator
