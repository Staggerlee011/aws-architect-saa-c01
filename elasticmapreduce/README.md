# elastic mapreduce

- hadoop service
- s3 (read from or  push to hdfs)
  - allows for emr cost to just be on processing rather storage
- auto scaling
- spot instances
- bootstrapping (allowing to customize hadoop cluster)
- attach preconfigured frameworks S
- scalability

## hadoop basics

- master node and slaves
- slaves can be core or task
  - core
    - stores data (hdfs)
    - must have at least 1!
  - task
    - runs compute tasks (can be used as core node)
    - optional

## phases of map reduce

- map phase
  - splits data into secitions to be processed
  - 128mb block size
- reduce phase
  - takes output of mapper
  - puts into single solution

![alt text](pic/phases.png "hadoop mapreduce phases")

[home](../README.md)