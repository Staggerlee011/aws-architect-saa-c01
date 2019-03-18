# s3 (simple storage service)

- regional
- durably via replicating to all az in region 
- durable via hash checking for corruption /  change
- paid by gb and puts / gets
- versioning
- no  max limit to total size
- 5tb max file size
- encrypt at rest (tde)
- host static webpages
- origin for cloudfront
- hybid backup option with aws storage gateway

  
## components
-  bucket 
    - containers for objects
    - no uppercase or underscores
    - allowed lowercase, numbrs and hyphens (periods for static webpages)
    - soft 100 bucket limit per account
    - regional
- s3 objects
    - can be made public via url
    - sub-name (folders)
    - every object can have metadata (header value )
    - every object can have tags
    - encryption
        - can be done at bucket level
        - at object level
        - sse-s3 (s3 managed keys)
        - sse-c (customer provides key)
        - sse-kms (uses key in aws kms)0
    - s3 select
        - works for csv and json
        - allows for reading parts of file based on sql like query
  
## features
- versioning
    - defined at bucket level
        - if enabled deleted objects are recoverable
        - if disabled deleted objects are gone
    - one way (once enabled unable to stop)
    - allows fro cross-region replication
        - allows for fault tolerance
        - works with encrypted files to
- storage classes
    - standard
        - default option
        - most expensive
        - 11 nines durability 
        - 4 nines availability
    - s3-ia (infrequent access)
        - used for none changing objects that are not used often but need quick access
        - access fees are greater but storage fees are less
        - 11 nines durability 
        - 3 nines availability
        - 30 days min charge for hosting an object
    - s3 one zone-ia (one zone infrequent access)
        - none critical objects single zone
        - 11 nines durability 
        - 99.5 nines availability         
        - 30 days min charge for hosting an object
    - glacier
        - long term storage
        - may take several hours to access file
        - access files from storage request (cant use url etc)
        - chepest storage type
        - 90 days min charge for hosting an object
- lifecycle policies
    - transition 
        - move objects to difference storage classes
        - based on creation date only
        - transition example
            - when added store in standard
            - after 30 days after creation move to s3-ia
            - after 90 days after creation move to glacier
    - expiration
        - delete objects
        - defined for current and previous versions
        - based on creation date only
        - cannot enable clean up explired objects delete markers if you enable expiration
- event notifications
    - allows events based on s3 objects
    - connects to
        - sns
        - lamdba
        - sqs queue
    - rules based on 
        - suffix
        - prefix
- permissions
    - 3 layers of permissions
        - iam
            - typical access via groups etc
        - bucket policies
            - same as ec2 polices
            - allows to lock down ip address 
        - access control lists   
            - allows access from different aws accounts

## static web hosting
- make bucket public
- must be enabled
- allows html, css, javascript
- common usage dr
    - bucket needs to be same name as website (www.mywebsite.com)
    - update route53 to failover for record set
- host website files (javascript files, css etc)
    - needs to set up cors (cross-origin resource sharing)
    - cors set in permissions for the bucket
  
## glacier
- archive storage (called vaults)
- cheapest storage
- encrypt on by default 
- api use ssl/tls endpoints
- lock vault
    - stops possibility of changing content for a period of time
- resotring
    - define how long the object is restored for 
    - price for reteral changes depending on
        - expedited (1-5 min)
        - standard (3-5 hours)
        - bulk (5-12 hours)
  
## transfering data to s3

- website gui 
- multipart upload 
    - splits large file to parts to allow for network failures
    - required for 5gb or larger
- s3 transfer acceleration
    - enabled at bucket
    - uses cloudfront edge locations
    - change endpoint to achive
        - from mybucket.s3.amazonaws.com 
        - to mybucket.s3-accelerate.amazonaws.com

### snowball
- snowball
    - transfer large (tb) of data from inhouse to aws
    - aws sends device to copy files to, ship  to aws and get upload
    - up to 80tb per device (pb solution)
- snowball edge
    - 100tb device
    - use compute to start migration during changes
    - cluster devices
    - run lambda functions run from device
- snowmobile
    - exabute scale
    - actual truck gets sent to you to copy data to!

## storage gateway
- connects to inhouse system via software vpn
- allows to alias to ebs
- encryped at transite and at rest
- connects to
    - vmware
    - hyper-v
    - etc
- volume gateway
    - ebs snapshots for dr
    - gateway-cached volumes
        - attach storage to physcial server(20% of perdicted storage) 
        - used for caching
    - gateway-storated volumes
        - storage gateway just takes snapshots 
        - acts as backups
- file gateway
    - gives file access from s3 to files 
- tape gateway
    - emulates iscsi tape
    - works with applications like veeam, vertias, arcserve, dell)

  
[home](../README.md)