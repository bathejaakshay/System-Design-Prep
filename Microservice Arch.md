#### Monolith vs Microservice Architechture

A monolithic application is built as a single unified unit while a microservices architecture is a collection of smaller, independently deployable services.
Although monolithic services can be scaled horizontally but they still are unified unit.

Microservice is a single business unit, all data and functions that are relevant to a service are put into one service, if it is separable.
- We can even have only three microservices which talk to their own dedicated databases
- The client maynot be directly talking to the microservice instead to the gateway which in turn talk to the microservices.


Adv of Monolithic services
- Good for small and cohesive team.
- The system is less complex and it needs comparatively less server maintainence.
- Less duplication as all the code resides in one service.
- Procedure calls are faster as compared to RPC (Remote procedure calls).


Disadv of monolithic:
- If there is a new member in the team, they need a lot of context on what they are developing. As the whole
- Main disadvantage is complex deployment, even a small change in the code will require the whole code to be deployed again.
- Not decoupled
- Single point of failure


Adv of Microservices:
- Easily scalable
- A new member can easily under the code of a particular microservice
- Testing is easy and easily deployable

Disadv of microservices:
- Needs skilled Architect
- RPC calls
