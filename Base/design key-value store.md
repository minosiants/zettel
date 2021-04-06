202103300930
Tags: #book #design #interview #B08B3FWYBX
__
# Design key-value store

 ### distributed  key-value store 
 `CAP` (Consistency , Availability, Partition tolerance)
 
 - `Data partition` - consistent hashing is a good chose (server is placed on the ring, key's hash placed on the ring as well and stored in the first server by clockwise)  
- `Data replication` 
- `handling failures`  - gossip protocol  

### summary 

 goal/problem | technique 
---------- | ---------
Ability to store big data| use consistent hashing to spread the load across servers
High availability | Data replication. Multi-data center setup  
Highly available writes | Versioning and conflict resolution with vector clock (gossip protocol) 
Data set partition | Consistent hashing 
Incremental scalability | Consistent hashing 
Heterogeneity | consistent hashing 
Tunable consistency | Quorum consensus 
Handling temporary failures | Sloppy quorum and hinted handoff 
Handling parmanent failure | [Markle tree](https://en.wikipedia.org/wiki/Merkle_tree)  
Handling data center outage | Cross-data center replications 





__
### Zero-Links
-

__
### Links
- 

 
 