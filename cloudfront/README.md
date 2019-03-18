# cloudfront

- cdn
- static 
- edges (100+ locations)
    - hosts route53 
    - aws waf rules
    - aws sheld
    - lamdba
- origin (source)
    - s3 
    -  elb
    - public http endpoint
- cache behaviour
    - defined by http header, if not defined uses TTL
    - define what to cache with path (images/*.jpg)
    - define lifetime of objects (min max default) 
        - TTL 0 always check for updated object
        - TTL 10 
    - query string
    - supports get, post, put, head
        - upload or send requests to a origin via an edge 
    - security
        - ssl certs
        - end to end https
        - waf
        - distribute private content
            - s3 (oai (orgin access identity) only)
            - get url / signed cookies (have expiry, restricited ip, trusted pairs)
- regional cache (saves rejected content from edges)
- point full domain at cloudfront to speed up dynamic
- performance
    - file size  
    - TTL 0
    - 
  
[home](../README.md)