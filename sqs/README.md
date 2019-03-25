# sqs (simple queue service)

- pull service
- decouples components
- ha queue (mulitple copies to ensure message not lost)
- max message size 256 of text
- can enable messages at rest
- cloudwatch can monitor message queue length (notify or scale out)

- queue types
  - standard queue
    - order is not guarenteed
    - guarantees each message will be delivered
    - possibly mulitples of same message delivered
    - nearly unlimited messages per secondS
  - fifo (first in first out)
    - ensures order of messages is kept
    - no duplication
    - up to 300 messages per second

- polling
  - each time sqs tries to get a message you are charged
  - long polling (1-20 sec)
    - polls for message randomly between 1-20 secs (message must be kept alive to be read during wait!)  
  - short polling
    - constant polling for message (can become expensive if messages are not requent)
  
[home](../README.md)