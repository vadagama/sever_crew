## ADR-8: Notifications

### Date:
2021-10-30

### Status:
Proposed

### Context:
The Farmacy Family system will generate several types of notifications to users via mobile application, email, and SMS services. Notifications include new recommended posts, messages from dieticians and doctors, health recommendations, reminders and invitations during the eLearning process. 

### Decision:
We are supposed to use one service to handle the responsibility of generating and sending different types of notifications. The Farmacy Food system uses [Amazon Simple Notification Service](https://aws.amazon.com/sns/) for this purpose and we don’t see any reasons not to reuse it for our project.