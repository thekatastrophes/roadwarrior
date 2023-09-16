# Style

[Home](../README.md) > [Architectural Approach](../README.md#architectural-approach) > Style ( [Previous](./1-characteristics.md) / [Next](../3-solution-design/1-actors.md) )

The architectural design of the proposed solution has been significantly influenced by several key factors, aligning with the unique characteristics of the startup venture and the nature of the product. These factors combined with the driving architectural characteristics have guided our decision-making process and led to the adoption of an approach that best suits our specific needs.

## Evolutionary Architecture
Our architecture should adapt swiftly to market changes, maintaining agility, and minimizing disruptions during development while providing a strong growth foundation.

## Leveraging Cloud Solutions:
Developing a cloud-native offers simplicity, scalability, and cost savings. It lets you focus on your core business and adapt to changing needs without large upfront infrastructure investments.

## Resource Constraints and Small Team Dynamics:
We prioritize efficiency and cost-effectiveness for startups. Our solution is designed for execution by a compact, skilled team proficient in cross-platform development, optimizing resource use for quality product delivery.

## Leveraging Established Solutions:
To address resource limitations, we leverage established technologies and products for non-specialized areas. This allows us to benefit from top-notch solutions like AI frameworks for mail parsing and notification systems without extensive in-house development.
As an initial design choice, we selected Event Driven Serverless Microservices as an architecture style. The details of our decision are explained in [ADR1: Use Event Driven Serverless Microservice Architecture](4-decision-records/adr1-use-event-driven-serverless-microservice-architecture.md). 


