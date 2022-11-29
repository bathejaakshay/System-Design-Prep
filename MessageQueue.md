#### Introduction
If we design something like Pizza outlets say P1, P2, P3 then we must have a persistent and asynchronous Queueing system to maintain the order of the incoming pizza request and divide them accordingly to different pizza outlet servers.
 
Properties:
- Asynchronous: User doesnt have to be engaged all the time after putting request into the queue system.
- Assignment or Notification: Queue system should give notification of the assignment of order to the resturant and its progress.
- Load Balancing: Avoid assigning the same job to multiple pizza shops using consistent hashing.
- A heart beat: Keep a heart beat function implemented, that asks every server after every few unit of time if its awake or not. If not then distribute its job to other outlets.


