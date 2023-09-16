# ADR3: Use hybrid technology for mobile app

[Home](../README.md) > [Decision Records](../README.md#decision-records) > ADR3: Use hybrid technology for mobile app ( [Previous](./adr2-use-an-existing-email-processing-service.md) / [Next](./adr4-do-not-implement-shared-caching.md) )

## Status

* Adopted (14/09/2023)
* Proposed (14/09/2023)

## Context

Road Warrior will deliver the richest user interface possible across all deployment platforms, offering a seamless and engaging user experience. We think richest but simple user interface that will set the application apart from the competitors. When we say simple, we think GMAIL like.

To improve the user engagement and deliver relevant information, the mobile app will utilize the geolocation service and support push notifications.

## Evaluation Criteria

* Cross-Platform Compatibility: The solution should work on web and all mobile platforms.
* Maintainability: The solution should allow for future enhancements.
* User experience: A highly responsive intuitive UI/UX leveraging geolocation functionalities is vital.
* Feasibility: Minimizing development time is important for a startup.

## Options Considered

### Option 1 - Native app

* Cross-Platform Compatibility: Separate apps should be developed for each specific platform.
* Maintainability: Allows for future enhancements but might be complex to maintain.
* User experience: Native apps can offer more polished user experience.
* Feasibility: More development effort is required for native apps.

### Option 2 - Hybrid app

* Cross-Platform Compatibility: Shared codebase can be used for the targeted platforms.
* Maintainability: Allows for future enhancements and is easier to maintain.
* User experience: It might be slightly compromised in performance compared to native apps.
* Feasibility: Fast development time and bigger development efficiency. Same web technologies can be used as the web app.

## Decision

* Use hybrid app approach for developing the mobile app.

## Implications

### Positive

* Richest user experience is supported
* Reduce development time and cost by using a shared codebase that runs on multiple platforms.
* Access to native features like GPS, push notifications and subscriptions.

### Negative

* Potential challenges in achieving platform-specific features, but it is not required to use any sensors other than GPS.
* Performance optimization is challenging. However, we don’t expect heavy operations happening in the mobile app itself.
