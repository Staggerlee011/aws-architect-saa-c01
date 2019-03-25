# hybrid environments and vpc peering
connecting on-prem to aws.  

## vpn

- one virtual private gateway per vpc (like igw)
- virtual private gateway gives 2 ip address for redundency 
- each subnet will need a route table to link to 
- only connects to a single vpc
- customer gateway (hardware vpn)
    - install phy device / software app on prem that acts as an connecter.
    - creates a public ip to connect to 
    - dynamic routing
        - bgp (border gateway protocol)
        - asn (autonmous system number)
  
## aws direct connect
- fiber from you on prem to aws
- 1gb / 10gb connection speed
- can share a direct connect with other companies 
- connect to virutal private gateway
- connect to vpc and public services (dynamodb / s3 etc)
- cost can be cheaper than internet vpn 
- more secure than vpn 
- use portal to get started with process (will need to pick a region )
- direct connect gateway
    - connects to all regions (except china)
    - ip address cannot be the same in any vpc 
  
## vpc peering
- example usage (active directory)
- ip address cannot be the same in any vpc
- 1 hop (cannot connect vpc 1 to vpc which connects to on prem)
- update route table (add cidr block for destination vpc peering connection as target) for both vpc
- update security rules for both vpcs
- peer vpc in same region or different regions
- peer vpc from different accounts / subscriptions
- connect to vpc or specific subnet(s)


  
[home](../README.md)