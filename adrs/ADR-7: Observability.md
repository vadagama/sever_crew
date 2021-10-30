#### ADR-7: Observability

**Date**
2021-10-29

**Status**
Proposed

**Context**
Making the Farmacy Family system observable gives developers and DevOps visibility and insight into their applications, as well as context to the infrastructure, platforms, and client-side experiences those applications support and depend on. With this information they can:
* Detects outages, software bugs, unauthorized activity, and service degradations.
* Report on the health of the system by measuring performance and resources.
* Understand how neighboring or dependent services might impact each other.
* Find unknown unknowns that have never occurred in the past.
* Identify long-term trends for capacity planning and business objectives.

**Decision**
We propose to use the same approach for logging, tracing and monitoring as for the Farmacy Food solution designed by the ArchCollider team - [https://github.com/ldynia/archcolider/blob/master/4.ADRs/003%20Tracing%20and%20Monitoring%20Sytem.md](https://github.com/ldynia/archcolider/blob/master/4.ADRs/003%20Tracing%20and%20Monitoring%20Sytem.md)

This ADR provides weighty arguments in favor of a DataDog solution vs ELK, Grafana and Amazon CloudWatch. There is no reason to change this approach. You could just connect new event sources to the Amazon Kafka Amazon Managed Streaming for Apache Kafka and set up new DataDog agents and metrics, alerts and notifications.