# performance

    `the ability to use computing resources efficiently to meet system requirements and to maintain that effcienct as demand changes and technology evolve`

## design princeipals

- democratize advanced technologies (see if saas / paas is availble over creating your own)
- go global in minutes 
- use serverless architectures
- experiment more often
- mechnical sympathy

## best practices

### selection

    `choosing the right instance and storage options`

- auto scaling is good!
- offload static content to s3
- use nosql instead of relational when needed

### review

    `re-evaulte when aws announces new features and services`

- keep up to date with aws
  - blogs
  - podcasts

### monitor

    `verify resiyrces oerfirn as expected`

- monitor and alert
- use lambda for actions

### tradeoffs

    `consider caching and read replicas`

- look at elasticache for data caching
- look at cloudfront for website caching
- look at snowball for data migrations to aws
- look at rds read replicas

[home](../README.md)