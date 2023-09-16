# Technology Stack

[Home](../README.md) > [Additional Considerations](../README.md#additional-considerations) > Technology Stack ( [Previous](./1-deployment-and-operation.md) / [Next](./3-engineering-practices.md) )

The architectural design we have developed is technology agnostic. We believe to make the proper selection of technologies you need to consider the budget, time to market, and the capabilities of the development team, which now are unknown. Rather than proposing specific technologies, we offer criteria for selecting the most suitable technologies, along with a few recommendations:

Cloud Providers: The choice of a cloud provider will be mostly influenced by factors such as cost considerations. However, we recommend considering well-established, globally recognized cloud providers like AWS, Azure, and Google Cloud mainly because of their geo-replication and serverless infrastructure. If the tech analysis requires to choose other cloud provider, they should offer essential features such as geo-replication, content delivery networks (CDN), and support for serverless infrastructure.

Front-end Frameworks: For a hybrid mobile application that shares the same source code as the web application some of the technologies you can consider include: React Native, Flutter, and others.

Serverless Microservices: The selection of serverless microservices will depend on the chosen cloud provider. AWS Lambda and Azure Functions are two suitable options to consider.

Event Broker: The choice of an event broker will also be contingent on the selected cloud provider. Options include Azure Event Grid, AWS EventBridge, and Google EventArc.

Backend Frameworks: Given that most of the microservices involve CRUD (Create, Read, Update, Delete) operations, a variety of backend frameworks can be employed. The decision should be influenced by the development team's familiarity and expertise with a particular framework.

Email Integrator: We recommend utilizing existing APIs for email retrieval and parsing. In the event that custom development is necessary, you can consider alternative development with Python in combination with mail parser libraries and natural language processing (NLP) libraries such as spaCy or NLTK.

Data Analytics: we recommend leveraging cloud-based analytics tools like AWS Athena, Google Data Studio, or Azure Machine Learning.

Testing and Quality Analysis: As the rich user experience and seamless rendering on all devices is essential for this application, we recommend using tools that enable cross platform and cross browser automation testing such as BrowserStack and others.
