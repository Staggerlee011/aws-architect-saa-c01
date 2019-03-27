# disaster recovery patterns

- think rto, rpo
- patterns below go from cheapest to most expensive
- patterns below go from worst rto/rpo to best

## backup and restore

- backup to s3 (for long term look at glacier)
- backups to different region
- save ami in recovery regions
- cloudformation templates for restores

## pilot light

- cross region replication
- keep recovery region as smaller instances
- turn off instnaces that are not needed in recovery region
- databases having read-replicas to promote
  - rds
  - dynamodb
- set up route 53 with failovers etc
- scale up instances for dr
- set dbs to primary

## low capacity standby

- cross region replication
- similar to pilot light
- set dbs to multi master (aurora)
- continous testing of recovery region
- route 53 weighted routing (traffic to 95% primary 5% recovery region)
- use autoscaling in secondary

## multi-site active active

- cross region
- multi master
- route 53 weighted routing (50%/50%)
- auto scaling everywhere
- either region can go down and service continious

[home](../README.md)