## Imagine you have recently opened up a new pizza parlor with one chef. What are the key points to scale the business?

1. To optimize the processes and increase the throughput using the same resource
    - Basically for a small scale business, instead of hiring multiple chefs we can pay more to one chef and get more work done. (Vertical Scaling)

2. Preprocessing at non peak hours as we do not want to load the system at peak hours
    - preparing pizza bases at non peak hours so that our chef is more efficient at peak hours 
3. Keep backups and avoid single point of failures. 
    - Now if one day the chef calls in sick then the business for that day is lost. So, we keep an emergency backup chef whom we pay only when primary aint available.
4. In case of scaling up the business, hire more full time chefs (Horizontal Scaling)

## Now we talk about EXPANSION of our Business.
 
Say we have 3 groups of chefs two of which are trained in pizza and third in garlic bread. Now if we have 2 types of incoming orders i.e pizza and garlic bread.  
How should we route them.  

5. Microservice Architecture  
   - Assign the garlic bread order to group of chefs specialized in garlic bread and pizza to pizza groups. Here we are dividing reposibility and will be scaling three groups differently.


But what will we do in case of electricity outtage or shop inoperability?  

6. Distributed System (Paritioning)
    - Open another shop shop as a backup where we can route the orders for that day.
    - Also orders local to second shop should be served by itself (Partioning)


#### Now consider you have two Pizza shops, delivery agent and a customer. Now where should customer place the order, shop1 or shop2?

7. Load Balancer
    - Customer place order with a central unit (load balancer) which in turns find out the shortes ETA for both the shops and place the order accordingly.

#### Now our system is fault tolerant but how do we make it flexible to change? e.g if we want to change the shop from just pizza to all other cuisines then do we need to do all above steps again?

For delivery agent and customer its just a shop, doesn't matter pizza or anything else. So we have separating of responsibilities here.

8. Decoupling the system
    - Separation of responsibilities, so that the system is flexible to change in future.
 
9. Logging and metric evaluation (audit logs of cutomers, delivery agents, orders etc for better analysis)

10. Extensible: We dont want our system to be product dependent i.e the item can be burger in future instead of pizza but it should still work the same.

