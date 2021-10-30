## ADR-10: Cloud provider

### Date:
2021-10-30

### Status:
Proposed

### Context:
The chosen architecture style: service-based architecture - implies that there will be several deployment units. The solution is designed for horizontal scalability, so we want to use features such as load balancing and load-based scaling. We would also like to use some solutions for managed databases. We tolerate multi-user rentals and other consequences of cloud solutions.

So, there are no reasons not to deploy our solutions to Amazon Web Services cloud as for the Farmacy Food solution.

### Decision:
* Deploy application components as well as databases to an AWS cloud.
* Reuse Farmacy Foods services such as 
* Consider AWS as a cloud provider for our services

### Consequences:
* Utilize solutions from Farmacy Food project
* We are getting cost-efficient and stable infrastructure platform with ability to scale
* New development and delivery pipelines will be setup for new services

For deployment view look [deployment](#heading=h.1lcn3p400er6) chapter.