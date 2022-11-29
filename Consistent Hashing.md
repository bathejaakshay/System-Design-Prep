#### Why Hashing?
- In a large scale distributed system, the data doesn't fit on single server. So it has to distributed among different machines also known as horizontal scaling.
- To have good performance, it is important that data is distributed evenly across these servers.
- We use hashing to uniformly distribute data among different servers. ( Hash(key)%N ). Firstly we perform hashing like md5 to distribute data across a numeric range evenly.
- Then we perform modulo **num_of_servers** operation on this hash value to distribute among them among N servers.
- As long as the number of servers stays the same, the object key will always map to the same server.  
- This type of Hashing is only good when number of servers is fixed.

#### Limitation of Hashing
- Whenever a server is added or removed from the cluster, even thought the Hash value is same but modulo N (number of servers) changes.
- This has drastic impact as we need to redistribute most of the keys again.
- Consistent hashing resolves this issue.


#### Consistent Hashing
- The goal of consistent hashing is that we want the mapping of data object to a server to remain same even though new servers are added or removed.
- In this type of hashing we hash both object and server name with the same hashing function to the same range of values. Also the we connect both ends of the hash space to make it a ring or circular hashmap
- Using a hashing function we hash each server by its name or IP address and place them on the ring.
- Then we hash each object by its key using the same hashing function. Here we dont use any modulo function.
- Now we go clockwise in the ring for each data object and assign the next appearing server to it. 
- Now whenver we add a new server only few data objects would need to be reassigned that comes directly before the new server.

#### Limitation of Consistent Hashing
- We do not get perfect partitioning/ distribution among the servers with equal size segments. (Non-uniform distribution).
- This problem occurs when servers can and go very frequently even though the servers were equally spaced initially.


#### Fixing the Limitation of Consistent Hashing using virtual nodes.
- For each server add multiple virtual nodes(servers) at different locations using hashing.
- In this distribution, each server handles multiple segments in the ring. i.e each virtual server handles a segment. (segment means data key objects coming directly before that server.)
- segment is the distance between any two vitrual servers.
- As the number of virtual nodes increases the ditribution of objects become more balanced.

Amazon DynamoDB and Apace Cassendra use Consistent Hashing to parition data.
Content Delivery system uses this to distribute content evenly
load balancers use this to distribute persistent connection evenly.


