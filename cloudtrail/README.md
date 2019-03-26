# cloudtrail

- monitors api calls to aws
- not enabled by default
- monitor events
  - all
  - read-only
  - write-only
  - none (data related events like s3 changes, lambda )
- stored in s3
- creates json files
- encrypted b y deafult

## cloudwatch intrigration

- extract metrics from logs of cloudtrail
- set up notiifcations of change with cloudwatch
- monitor failed login attempts
- failed api authorization
- iam changes

[home](../README.md)