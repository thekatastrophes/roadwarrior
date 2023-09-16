# Front End Technology

[Home](../README.md) > [Solution Design](../README.md#solution-design) > Front End Technology ( [Previous](./6-data-storage.md) / [Next](./8-security.md) )

The web application and the mobile application will be developed using a front-end framework that enables developing hybrid mobile applications, as explained in [AD3: Use hybrid technology for mobile app](../4-decision-records/adr3-use-hybrid-technology-for-mobile-app.md).

The user interface will be compliant with the latest W3C standards. It will be based on responsive design, that serves the content to multiple devices from the same codebase, making it easily maintainable. The application will be identical on the latest version of the most used browsers and mobile phones.

We've opted not to adopt a caching mechanism as part of the overall architecture, for reason mentioned in [ADR4: Do not implement shared caching](../4-decision-records/adr4-do-not-implement-shared-caching.md).
