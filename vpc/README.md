# vpc
## network terms 
  
stateful - is an inbound rule that includes the return network traffic even if its on a different port (security groups)  
  
stateless - is an outbound rule only. if you have return traffic you will need to create rules to allow this as well! (network acl)
  
## aws network topology
igw -> route table -> nacl -> security group -> ec2 instance

## vpc
- regional 
- default vpc created has a igw
  
## route tables
- set to vpc
- define network traffic routes
  
## internet gateways (igw)
- must be created
- gives access to internet to vpc
- 1 per vpc 
  
## network acl (nacl)
- stateless
- set to vpc
- rules have order (bp raise in 10s)
- nacl are queried before security groups 
- assigned to subnet(s)
  
## security groups
- stateful
- set to vpc
- no ordering of rules
- processed after nacl
- assigned to objects (ec2 instances) not subnets, 
- objects do not have to be in the same subnets
- can have multiple security groups assigned to the same object (all processed at once still)
  
[home](../README.md)