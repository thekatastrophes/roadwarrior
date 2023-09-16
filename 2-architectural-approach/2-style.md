# Architectural Style

[Home](../README.md) > [Architectural Approach](../README.md#architectural-approach) > Style ( [Previous](./1-characteristics.md) / [Next](../3-solution-design/1-actors-and-actions.md) )

We have based the architectural design of our proposed solution on several key factors that align with the unique characteristics of the startup venture and the product's nature. These factors, in conjunction with our driving architectural characteristics, have steered our decision-making process. 
Here are the architectural styles we have selected and the additional four factors that have significantly influenced our choice:

# Architectural Style: Event-Driven Serverless Microservices

- **Evolutionary Architecture:** Our architecture prioritizes adaptability to swift market changes, maintaining agility, and minimizing disruptions during development while providing a strong foundation for growth.
- **Cloud Native:** We've chosen a cloud-native approach to offer simplicity, scalability, and cost savings, allowing us to focus on our core business and adapt to changing needs without substantial upfront infrastructure investments.
- **Resource Constraints and Small Team Dynamics:** Emphasizing efficiency and cost-effectiveness for startups, our solution is designed for execution by a compact, skilled team proficient in cross-platform development, optimizing resource utilization for quality product delivery.
- **Leveraging Established Solutions:** To address resource limitations, we harness well-established technologies and products for non-specialized areas, enabling us to benefit from top-notch solutions like AI frameworks for mail parsing and notification systems without extensive in-house development.

Details of our decision regarding this architectural style can be found in [ADR1: Use Event Driven Serverless Microservice Architecture](../4-decision-records/adr1-use-event-driven-serverless-microservice-architecture.md).
