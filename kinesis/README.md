# kinesis

- real time processing of big data
- parallel processing (pass data to multiple destinations)
- billed by shard hours
- processes data from iot for example
- passes to elastic map reduce, redshift, s3, dyanmodb etc
- steam contains shards (1mb/sec in 2mb/sec out)
- producers (things that pass in data)
  - iot sensors
  - api
  - if data larger than 1mb then need more producers
  - create producers with java library
  - can install agent to linux boxes
- consumers
  - pushes data to service
    - redshift / emr etc
    - consuer library (java) to create own comsumer

## kinesis video stream

- takes vidieo steaming data

## kinesis data streams

- standard data loading
- encrypts data
- max 7 days of data (default 1 day)
- pass to emr

## kinesis firehose

- load and save data
  - s3
  - redshift
  - elasticsearch
  - splunk etc

## kinesis data analytics

- run sql queries against data
- save outputs to data stream or firehose

[home](../README.md)