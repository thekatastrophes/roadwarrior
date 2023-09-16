# ADR4: Do not implement shared caching

[Home](../README.md) > [Decision Records](../README.md#decision-records) > ADR4: Do not implement shared caching ( [Previous](./adr3-use-hybrid-technology-for-mobile-app.md) / [Next](./adr5-use-geo-replication.md) )

## Status

* Adopted (15/09/2023)
* Proposed (15/09/2023)

## Context

While building and analyzing the architectural design we needed to decide whether a caching mechanism is required to address latency and performance that might potentially affect the responsiveness and the first contentful paint.

## Evaluation Criteria

The solution must be capable of achieving response time from web of 800ms and for mobile, first-contentful paint of under 1.4 seconds.

## Options Considered

The options are either to implement shared-caching technologies in the initial architecture or not. Caching will generally speed up any application and is usually based on frequently accessed data. For this application most of the data provided by the services will be the actual trip information and given the large number of users this does not map particularly well to a frequently used cache. What may be a relevant type of caching is to pre-compile information e.g., when trip information is updated precompile all trip information for that user into pages of JSON data (or similar) that would be directly supplied to individual requests. This would save the cost of any joining or searching queries, remove any marshalling costs, and remove any compression costs. The negative impact of adding caching is generally financial cost and a small overhead of complexity.

## Decision

Whilst caching (or more explicitly pre-compilation) could have substantial impact it is ultimately felt that the architecture is capable of being sufficiently performant without this overhead. Additionally, adding caching at a later stage would not require rethinking architecture but would for the most part be an optimizing addition. For these reasons and for the sake of cost savings, we have selected to omit shared-caching technologies at this point.

## Implications

### Positive

* 800ms / 1.4 second evaluation criteria are achievable without caching. This assumes well designed service interactions that selectively load only what is needed for immediate display, coupled with deferred loading for data just before it is needed.
* Saves cost and a small amount of complexity.
* Caching can be added in a relatively disruption free manner at a later stage if monitoring suggests this is needed. If this is required, revenues are likely to be more available to support its introduction.

### Negative

* Adding caching at a later stage (if needed) will incur a small additional cost / disruption.

### Risks

* Initial deployments are not sufficiently performant. If this is allowed to occur a poor user experience could significantly impede take up. It is important that load testing is performed prior to go live to ensure performance metrics can be achieved. Soft go live may be a useful strategy to consider.
