## ADR-2: Service-based architecture style approach

### Date:
2021-10-24

### Status:
Proposed

### Context:
The current Farmacy Food system style is a modularised monolith system with all components in a single deployable service. This structure would have probably been chosen for its simplicity and cost efficiency.

This monolith structure is however causing the following business impact:
* Change is difficult, it takes too long and something else usually breaks.
* Hard to maintain, observe and test.
* It is hard to change the data structure, since it has multiple dependencies.
* Same service and database is used for different kinds of requirements i.e. for reporting and real-time transactions. This causes issues in both functionalities.

We believe that the functionality of the Farmacy Family system is more fragmented, but using a microservice approach is not advisable.

### Decision:
We see that different parts of the Farmacy Family system have different architectural requirements (quality attributes).



* The customer interacts with unified for Farmacy Food and Farmacy Family web and mobile applications also with web conferencing module UI (incorporated in main apps with APIs). These parts have to be usable and changeable to avoid customer frustration (see QA-5 and QA-5)).
* Another significant part of our system is the Social Network Module. It contains a lot of components which should be closely related to each other and it could be hard to maintain this with a microservice approach.
* Third part of our system is the Customer profile Module. It must be secure (see QA-4).
* Webinars Module should be usable and productive and we suppose not to infest in development in that case (You can read our arguments in ADR-4: Webinars capability)
* And finally we need eDietician Module, Inventory Replenishment Module and Analysis of Service Level Module. These modules are based on AI mechanics and should be modifiable and secure as well (see QA-10 and QA-11).

This makes it clear that we need to break the monolith. The communication between these modules needs to be both synchronous and asynchronous.

Evaluating the functional modules that need to be implemented, as well as the architectural principles that fulfil our functional and architectural requirements, we have two candidates: service based and microservice architecture.

Service-based architecture give us several benefits:
* macro-services resolves orchestration and transactional issues 
* allows for non-transactional orchestration of services 
* allows for protocol-agnostic heterogeneous interoperability 
* allows for transformation of contract differences 
* database scope improves performance due to fewer remote calls 
* refactoring entire database may not be feasible or possible

Also, there are some cons:
* change control becomes more difficult
* looser bounded context of services 
* tighter service coupling based on schema database scope 
* schema changes become expensive and difficult
* decrease in overall performance

This comparison is based on Neal Ford's presentation “Comparing Service Based Architectures”.

Microservices could add a lot of complexity than a space-based approach for development teams. Each microservice has its own API, which apps rely on to be consistent. For microservices architecture we have more pricey hosting infrastructure with security and maintenance support, and also development teams should be more skilled and expensive.

We suggest choosing a good compromise between monolith and microservices: space-base architecture style with holistic UI (Web and Mobile), event-based integration approach with Kafka service and central simple object storage for both Farmacy Food and Farmacy Family systems.

**Consequences**
* Quicker solution to compliance with our goals and requirements
* Comprehensible and manageable migration
* Much higher maintainability and testability leading to more stable system
* Manageable coarse grained services