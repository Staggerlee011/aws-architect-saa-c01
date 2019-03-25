# sns (simple notification service)
  
- push service
- publisher subscriber

- publishers
  - cloudwatch
  - most saas and paas from aws (s3 event, db event etc)

- subscribers
  - 10 million endpoints per topic (can be different types at the same time)
  - has retry logic that can be defined
  - sms
  - email (must confirm subscription to email address)
  - url
  - lamdba
  - sqs
  - http / https

- topics
  - max size 256kb
  - object you publish message to
  - subscribers, subscribe to topics
  - name must be unique with amazon resource name (arn)
  
## visual note

visual note for sns by Jerry Hargrove  
![alt text](https://www.awsgeek.com/images/Amazon-SNS-1553181286849.png "visual note for sns by Jerry Hargrove")

[home](../README.md)