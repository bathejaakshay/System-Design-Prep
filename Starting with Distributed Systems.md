Imagine you have recently opened up a new pizza parlor with one chef. What are the key points to scale the business?

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


6. Open another shop shop as a backup where we can route the orders for that day.

