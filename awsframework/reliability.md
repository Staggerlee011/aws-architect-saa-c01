# reliability

    `the ability to revoery from failure and mitigrate distrutptions`

## design principals

- test recovery procedures
- automatically recover from failure
- scale horizontally
- stop guessing capacity
- automate change

## best practices

### foundations

    `limit access, isolate resources, safegaurd applications`

- use iam for access control
- use vpc for work seperation (dev/prod)
- use trusted advisor (offers bp advice, shows service limits (max ec2 max))
- use aws shield (standard free version and paid for premium)

### change management

    `monitor aws apis, automatically scale, monitor key metrics`

- cloudwatch (see changes to access control)
- aws config (configuration awareness)
- cloudtrail (audit aws apis)
- autpo scaling (demand management)

### failure management

    `disaster recovery strategy, maintain backups`

- cloudformation (iac rebuild from scratch)
- s3 (durable backups)
- amazon glacier (durable archives)
- aws kms (key management)

  
[home](../README.md)