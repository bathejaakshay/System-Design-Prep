Imagine we have an application hosted on cloud service. Recently it has gotten a little popular and the load on the servers has increased.  
So how will you scale your system to match the user requirement?

We can scale up the system in two ways:
1. Vertical Scaling: Buy a more bigger system which serves all the user requests single handedly.
2. Horizontal Scaling: Buy multiple systems that together serve all the user requests.

#### Key Differences b/w Horizontal and Vertical Scaling:

|**Horizontal Scaling**|**Vertical Scaling**|
|:---:|:---:|
|Load Balancing Required| No load balancing required as we are using single server
| Resilient to failure as we have multiple machines to take over | Single point of failure |
| Network Communication (RPC) | Inter Process communication |
| Data Inconsistency | Data is always consistent|
| Scales well as users increase | There is always a hardware limit to how much you can vertically scale|

---

There is always a Trade off to which scaling to adopt for the use case.
In our case we can first start with vertical scaling and then if the users still increases by a lot we can further scale them horizontally with the bigger systems.
