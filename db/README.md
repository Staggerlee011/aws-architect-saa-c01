# dbs

## managed database services
### amazon rds 
- relational database
- can run the following:
    - sql server
    - mysql
    - postgres
    - mariadb
    - oracledb
    - aurora

### amazon redshift
- datawarehouse 

### dynamodb 
- document database

### amazon elasicache
- key-value database
- can run the following:
    - redis
    - memcache
  
### amazon neptune
- graph database

### elastic map reduce (emr)
- column database
- can run the following:
    - hbase
  
## amazon rds 
- scale up and down (shut down instance to upgrade) 
- can do primary, read-replica (except sql server / oracle)
- multi-az failover (synch instead of osync)
- sits in vpc subnet
- has a security group
- encrypt database at rest (tde)
- encrype snapshots cant move region (kms is regional)
- encryption at lunch only
- daily backups for 35 days (can do manual backups if needing longer)
- migration can be done with normal tools 
    - mysql = mysqldump
    - postgres = 
    - aws migration tool 
- can control when upgrades of version happen
- deleting db deletes standard backups only (manual backups are kept)


### aurora
- quicker than mysql (x5) / postgres (x3)
- continious backup (backTrack for point in time restore)
- quick replication to repoicas 
- up to 15 replicas (across 3 az)
- uses the same storage for replicas! s3 
- can have multiple masters 
- auroa serverless 
    - pay as you go (no user access will scale down and just charge for storage)
    - auto scales up and down

## dynamodb
- document db (json)
- dynamic scaling (storage and performance), based on read capacity and write capacity
- api only (serverless)
- fault tolerance via distributing data across all az in the region 
- can encrpyt at rest (tde)


[home](../README.md)
