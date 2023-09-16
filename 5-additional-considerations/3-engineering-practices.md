# Engineering Practices

[Home](../README.md) > [Additional Considerations](../README.md#additional-considerations) > Engineering Practices ( [Previous](./2-technology-stack.md) / [Next](./4-minimum-viable-product.md) )

## Xtreme Programming

Acknowledging the inherent uncertainty in the startup landscape, we are recommending Xtreme Programming (XP) principles. XP promotes short development cycles, ensuring rapid feedback loops. This agile approach enables to adapt swiftly to evolving requirements, a common occurrence in startup environments.

Additionally, the Xtreme Programming enables smaller teams to be more productive and efficient as well as self-sufficient.

## Testing and Quality Assurance

Considering that the Availability is one of the driving characteristics of the RoadWarrior, the testing strategy and the quality assurance must be considered from start, especially if we take in consideration that bugs caught early in the development process are less costly to be fixed than those found during testing and significantly less expensive than those caught in production. 

We suggest the following tests to be taken in consideration for automation: end to end automation, unit, integration, and contract tests. Tests at these levels provide faster feedback and build testability into the design of the code, which in turn allow for confidence to quickly be built in the form of a suite of tests that can be run on every commit and every build pipeline.

As the application needs to provide the richest user experience across different platforms and devices it is essential also to consider using a tool that can provide automatic tests across all platforms.

The performance and load testing must be considered as well from start as the application has a predefined requirements for responsiveness and number of users.

## CI/CD

Continuous Integration and Continuous Deployment (CI/CD) are fundamental practices in event-driven serverless microservices architecture, and they need to be considered from start.

Maintaining a consistent and reliable codebase is paramount in the event-based systems, so we suggest using a trunk based development. 

CI/CD promotes automated execution of unit and integration tests and can be configured to create visual dashboards for easier monitoring and health checks.

CI/CD enables implementation of automated deployment strategies like canary releases or blue-green deployments. This should not be considered from start but should be on the todo list as the product matures.

In serverless architectures, where resources are allocated on-demand, CI/CD ensures that only the latest and optimized versions of microservices are deployed, leading to efficient resource utilization and cost savings.
