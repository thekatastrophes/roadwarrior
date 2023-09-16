# ADR2: Use existing market mail poll service

[Home](../README.md) > [Decision Records](../README.md#decision-records) > ADR1: ADR2: Use existing market mail poll service ( [Previous](./adr1-use-event-driven-serverless-microservice-architecture.md) / [Next](./adr3-use-hybrid-technology-for-mobile-app.md) )

## Status

* Adopted (14/09/2023)
* Proposed (14/09/2023)

## Context

Road Warrior will proactively scan and filter travel-related emails, ensuring users have access to all relevant information in one place. Users can also whitelist or block certain emails to be processed or not processed by Road Warrior. Alternatively, users who would prefer not to give us access to their e-mails can instead forward e-mails to us for processing.

Road Warrior will enable automatic trip creation based on reservation details that users received on email. To achieve this, the emails that users have whitelisted or forwarded to the app need to be processed to extract the relevant information.

Road Warrior will be accessible and functional worldwide, catering to the needs of travelers across different languages, regions, and time zones.
We've crafted a product vision within the product statement that aligns with our understanding and vision for its application. Our primary objective in doing so is to emphasize that the true value and uniqueness of this solution lies not solely in the Mail Processing Technology, but in the product itself. That means that the email processing element is not likely to be an area we can differentiate our services through and is not identified as our key competency making outsourcing an attractive option. There are existing mail processing services that offer poll and mail parsing capability that meet our requirements.

## Evaluation Criteria

Feasibility; Adaptability; Data Accuracy; Data Privacy; Scalability.

## Options Considered

* Option 1: Utilize existing Email Processing Service.
* Option 2: Develop a custom Email Processing Service.

**Feasibility:** Existing market solution can save time and resources and shorten the time to market. For initial deployment the cost of using the service will be substantially less than the cost of developing this capability ourselves. Total cost for using the service will increase over time with usage but increased cost will only occur with increased success of our application which means finance will be available for this increased cost.

**Adaptability:** If our requirements change over time, using existing market service, will make us dependent on the third party adapting to these requirements. Vendor lock in may become an issue (potential conflict with price increases etc).

**Data Accuracy:** Established mail parsers been extensively trained and tested on a wide range of data, making them highly accurate in understanding and extracting travel-related information from emails.

**Scalability:** Having in mind that Road Warrior is targeting 15M users, that might be a huge challenge for an existing mail service and the scalability will be out of our control.

**Data Privacy:** Out of our control and will directly depend on the policies and standards of the chosen solution. Vetting suppliers and ongoing confirmation of compliance would need to be concerned. Topics such as modern slavery, bribery and corruption etc need consideration.

## Decision

* We will use mail processing services already available on the market.

## Implications

* Improved time to market
* Low initial cost
* We need to establish clear evaluation criteria when choosing the mail processing service (poll and parser) including considerations for accuracy and scalability.

## Risk

* We might not find a mail processing service that meets our requirements for accuracy, scalability or privacy/ security concerns. This would mean we would need to reverse this decision and create our own capability.
* In the long run we might need to switch to other existing poll mail services or decide to develop our own if our evolving requirements cannot be met or vendor locking / pricing becomes an issue.
