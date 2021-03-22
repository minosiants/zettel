202103221525
Tags:  #book #design #interview #B08B3FWYBX
__
# Design a rate limiter
The main idea is to have a counter that track the number of requests from the same IP address. 

- server side or client side ?
- standalone or integrated in the app

### Algorithms for rate limiting
- Token bucket   
- Leaking bucket   
- Fixed window counter  
-  Sliding window log  
-  Sliding window counter   

To make a user to be aware of the rate limit http headers are used.  
`X-Ratelimit-Remaining`  
`X-Ratelimit-Limit`  
`X-Ratelimit-Retry-After`  

      
examples : 
[Twitter rate limits:](https://developer.twitter.com/en/docs/basics/rate-limits)  
[Stripe rate limits](https://stripe.com/blog/rate-limiters)  
__
### Zero-Links
-

__
### Links
- 

 
 