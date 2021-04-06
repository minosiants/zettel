202104041632
Tags:  #book #design #B08B3FWYBX
__
# Design id generator in distributed systems 
### understand the problem and establish design scope

for instance 

- IDs must be unique 	
- IDs are numerical values only   
 - IDs fit into 64bit  
 - IDs are ordered by date  
 - Ability to generate over 10 000 ids per second		


### Propose high level design and get by - in 

- Multi master replication  
- UUID   
- [Ticket server](https://code.flickr.net/2010/02/08/ticket-servers-distributed-unique-primary-keys-on-the-cheap/)    
- [Twitter snowflake approach](https://blog.twitter.com/engineering/en_us/a/2010/announcing-snowflake.html)    


