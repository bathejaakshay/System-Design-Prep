#### Motivation

- Lets consider a microservice architecture. Lets say microservices A has to get a progress update from microservice B and B from C.
- Now if we use Request/Response method then A requests B and B requests C and they wait for the response.
- Now we C fails then we will have failure latency i.e it will take time for the reponse to reach A and change its data state.

#### Welcome PubSub

PubSub resolves this issue by adding message broker in between like Kafka. 
- Now A put msg on message broker and forgets about other stuff, B puts msg on broker. Now if c fails then msg broker will send the progress msg to C when it wakes up.
- In this way no body has to wait for anyone.
- So we publish event on msg broker and B and C subscribe to it.

Drawback:
Inconsistency.
