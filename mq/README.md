# amazon mq

- uses open source message queue
- can pull or push (queue or topic)
- cannot auto scale like sns and sqs
- runs apache activemq
  - compatable with jms api or protiocols such as amqp, mqtt, opernwire, stomp 
- allows for simplier migration than going to sns or sqs
- can enable automatic updates of minor updates to version
- security group needs port 8162 open
- broker
  - define size of ec2 instance
  - define if single instance or ha (cross az)
  
[home](../README.md)