# ADR6: Use a shared logging service for event correlation

[Home](../README.md) > [Decision Records](../README.md#decision-records) > ADR7: Use a shared logging service for event correlation ( [Previous](./adr5-use-geo-replication.md) / [Next](../5-additional-considerations/1-deployment-and-operation.md) )

## Status

* Adopted (15/09/2023)
* Proposed (15/09/2023)

## Context

Microservices and Event-Driven architectural styles both score very poorly on simplicity, this could have an impact on our uptime goals if there is an issue we need to trace.

We should use a logging system which supports our engineers in identifying the cause of problems and support their efforts in resolving outages quickly to support our high-availability targets.

## Evaluation Criteria

Each of the following criteria is in service of the availability characteristic for our system, ensuring we can isolate the cause of issues when they occur and reduce any downtime.

1. Support correlation of multiple operations via the associated event.
2. Gather logs from all components into a single point of access.
3. Avoid introducing further complexity and potential points of failure.

## Options Considered

### Option 1 – Storing logs on each microservice

* Poorest option for supporting event correlation and gathering of logs.
* Would have no impact on system complexity by avoiding any shared components.

## Option 2 – Service to scrape logs from individual microservices

* This would allow correlation and gathering all logs in one place whilst not introducing a dependency between components as they would be unaware of the scraper.
* Unfortunately, this would be difficult in a serverless infrastructure as we would need to ensure we scrape before the instance is torn down.

### Option 3 – Separate logging component, receiving logs via events

* Components raise log events into a shared location for correlation and reporting.
* This would work nicely with serverless infrastructure.

## Decision

We will raise log events from our microservices to a logging component for correlation.

## Implications

### Positive

* This will allow engineers to see how an event has been handled by multiple components and identify problems within the flow.
* Additionally, this provides an option for analysis of system performance and may allow engineers to identify issues before they impact our availability.

### Negative

* High network load would be worsened from logs events being raised; we can mitigate this by using a service that supports log sampling.
* Having a separate logging event may impact app performance, but technologies such as event buffering can mitigate that.
