# ADR5: Use geo-replication

[Home](../README.md) > [Decision Records](../README.md#decision-records) > ADR5: Use geo-replication ( [Previous](./adr4-do-not-implement-shared-caching.md) / [Next](./adr6-use-a-separate-logging-component-for-event-correlation.md) )

## Status

* Adopted (15/09/2023)
* Proposed (15/09/2023)

## Context

Road Warrior will be available internationally to users across multiple geographical regions. To ensure scalability, high availability and performance on an international scale we need to decide on using proper distribution technology.

## Evaluation Criteria

* Scalability: The system should be able to handle a large number of users and data across different geographical regions.
* Availability: The system should be highly available and provide continuous service internationally.
* Performance: The system should ensure responsive and low-latency experience for the users.

## Options Considered

### Option 1 - Single-Region Deployment

* Availability: Vulnerable to regional outages, impacting international users.
* Performance: Decent performance within the region but slower for users in distant regions

### Option 2 - Geo-Replication

* Availability: High availability with redundancy available across regions. The risk of regional outages is reduced.
* Performance: Improved performance for users in their respective regions.

## Decision

* We will use geo-replication in key global locations to ensure responsiveness to all user locations.

## Implications

### Positive

* Improved user experience and response time by services being available in the nearest geographical location to the user.
* High availability and redundancy internationally.
* Mitigated risk of regional outages.
* Can be done incrementally based on the usage of the application.

### Negative

* Additional cost associated with geo-replication.
