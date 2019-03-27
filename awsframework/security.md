# security

    `the ability to protect informatiom, systems and assets while delivering business value through risk asscessments and mitigation strategies`

## design principals

- implement a strong identity foundation
- enable traceability
- apply secuirty at every layer
- automate secuirty
- protect data in transit and at rest
- prepare for secuirty events

## best practices

### identity and access management

    `securely control access`

- use iam heavily!
- mfa!
- least privilage
- aws organizations
  - centrally managed accounts
- use roles for application secuirty (temp credientials!)

### detective controls

    `real time monitoring, access logging`

- cloudtrail! 
- aws config!
- cloudwatch!
- guardduty 
  - threat detection service
  - ml service
  - can use managed rule sets
  - uses
    - cloudtrail events
    - vpc flow logs
    - dns logs

### infrastructure protection

    `isolated private networks`

- keep public and private ec2 instances seperate (subnets)
- lock down developer accounts to environments
- amazon inspector
  - vulnerability dectection
  - installs agent on ec2
  - cis benechmarks
  - common vulnerabilities
  - can look at real-time behaviour during a scan
- aws shield
  - enabled by default
  - free by default
  - stops matformed tcp
  - ddos attacks
  - reflection attacks
  - layer 3/4
  - advanced (has cost involved!)
    - 24/7 incident responce team
    - set up advanced protection
    - give solutions for 
    - aws refund you for issues
- aws waf
  - includes aws shield advanced!
  - sql injection protection
  - cross site scriptiing
  - bad bots
  - high request rates
  - associate with 
    - cloudfront
    - application load balancers (alb)

### data protection

    `limit access, use encrpytion`

- amazon macie
  - ml for access to s3
  - alerts
    - on data events
    - non encrypted backups
    - signs of attacks
    - credentials in source code
- encrypt data at rest
- keep keys save (kms)

### incident response

    `incident response team, automate response`

- cloudformation
  - create scripts to
    - lock down environment if issues happen
    - limit access to only secuirty team

[home](../README.md)