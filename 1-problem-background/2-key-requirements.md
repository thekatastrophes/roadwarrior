# Key Requirements

[Home](../README.md) > [Problem Background](../README.md#problem-background) > Key Requirements ( [Previous](./1-problem-statement.md) / [Next](../2-architectural-approach/1-characteristics.md) )

In this section, we have distilled the requirements document, presentation content, and FAQ clarifications into our architecturally significant key requirements.

## Functional

| # | Context | Details |
| - | ------- | ------- |
| 1 | Email Integration | Road Warrior will proactively scan and filter travel-related emails, ensuring users have access to all relevant information in one place. Users can also whitelist or block certain emails to be processed or not processed by Road Warrior. Alternatively, users who would prefer not to give us access to their e-mails can instead forward e-mails too us for processing. |
| 2 | Real-time Updates | Our system will seamlessly interface with airline, hotel, and car rental providers, delivering travel updates such as delays, cancellations, gate changes, and more within 5 minutes of receiving the update. We aim to outperform competitors in delivering timely information. In future we should anticipate integrate with other interfaces (i.e., trains, bus lines). |
| 3 | Manual Reservation Management | Users will have the flexibility to manually add, update, or delete reservations, providing complete control over their travel plans. However, this is a supplementary flow – the main competitive edge remains the e-mail integration. |
| 4 | Trip Organization | Road Warrior will intelligently organize travel items by trip, automatically removing them from the dashboard once a trip is completed. This ensures a clutter-free and organized experience. |
| 5 | Social Sharing | Users will be able to share their trip information with ease by connecting with standard social media platforms or selectively sharing with targeted individuals. |
| 6 | Rich User Interface | The platform will deliver the richest user interface possible across all deployment platforms, offering a seamless and engaging user experience that takes full advantage of the platform it is deployed to. When trips are no longer relevant, they will be removed as to not interfere with the experience. |
| 7 | Support System | Where issues arise, we will facilitate contacting the travel agent associated with a trip (or a user definable fallback). Support will happen off-system, and we will not track this in-app. |
| 8 | Yearly Summary Reports | Road Warrior will provide end-of-year summary reports to users, offering a wide range of metrics about their travel usage. These insights will help users make informed decisions and optimize their travel experiences. |
| 9 | Analytical Insights | We will gather and analyze data from users' trips, offering valuable insights into travel trends, locations, airline and hotel preferences, cancellation rates, and more. This data will be used to enhance the user experience and provide personalized recommendations. |

## Non-Functional

| # | Requirement | Details |
| - | ----------- | ------- |
| 1 | High Availability | Users can rely on Road Warrior with a maximum of 5 minutes of unplanned downtime per month, ensuring constant access to their travel information. |
| 2 | Real-time Updates | Travel updates will be presented in the app within 5 minutes of generation by the source, guaranteeing up-to-the-minute information. |
| 3 | Responsiveness | Our platform will offer swift response times, with web response times of 800ms and mobile devices achieving a first-contentful paint of under 1.4 seconds. |
