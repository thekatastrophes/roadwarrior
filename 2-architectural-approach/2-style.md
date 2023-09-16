# Style

[Home](../README.md) > [Architectural Approach](../README.md#architectural-approach) > Style ( [Previous](./1-characteristics.md) / [Next](../3-solution-design/1-actors.md) )

The architectural design of the proposed solution has been significantly influenced by several key factors, aligning with the unique characteristics of the startup venture and the nature of the product. These factors combined with the driving architectural characteristics have guided our decision-making process and led to the adoption of an approach that best suits our specific needs.

## Evolutionary Architecture

Our architectural framework embraces adaptability and evolution. It has been designed to accommodate changes seamlessly, fostering the agility required to respond to market dynamics and shifting priorities offering fast feedback cycles. This evolutionary architecture minimizes disruptions during development while maintaining a robust foundation for growth.

## Resource Constraints and Small Team Dynamics

As a nascent startup with limited resources, we recognize the importance of efficiency and cost-effectiveness. Consequently, our solution is meticulously crafted to be executed by a compact, highly skilled V-shaped team capable of proficiently handling cross-platform development. This approach optimizes resource allocation and enhances our ability to deliver a quality product within our resource constraints.

## Leveraging Established Solutions

Recognizing that startups often operate with limited resources, our solution leverages well-established technologies and products for non-specialized areas. This approach ensures that we benefit from the best-in-class solutions, such as utilizing established AI frameworks for mail parsing and scanning or notification systems, without the need for extensive in-house development.

## Leveraging Cloud Solutions

In summary, our solution's architecture is a product of thoughtful consideration, tailored to address the unique challenges and opportunities that a startup environment presents. It emphasizes resource optimization, adaptability, and responsiveness, aligning perfectly with the ethos of our new venture. Through these design principles, we are poised to navigate the dynamic startup landscape effectively and deliver a product that stands ready to evolve with the market.
As an initial design choice, we selected Even Driven Serverless Microservices as an architecture style. The details of our decision are explained in [ADR001]. Upon working through the implications of this architecture style we didn’t find anything to contradict this selection so neither of the alternatives have been progressed.
