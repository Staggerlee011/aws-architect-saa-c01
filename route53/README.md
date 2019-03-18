# route 53
- dns service
    - register domains
    - dns (domain name to ip for internet)
    - health check (verify application is reachable)
- can point to elastic ips (s3 buckets / cloudfront etc) via alias records (cname)

  
### route 53 routing policy
- simple - all traffic to endpoint
- weighted - split traffic to different endpoints by %
- latency - split traffic to different endpoint by latency
- failover - have secondary endpoint if primary is down
- geolocation - defined by location
  
#### failover
- use s3 bucket for when website is down to host a simple http page
- s3 bucket must have the same name as the domain name

  
### dns basics
- a - ip4
- aaaa - ip6
- cname - hostname to hostname
- mx - email routing
  
[home](../README.md)