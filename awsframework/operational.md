# operational

    'the ability to run and monitor systems to deliver business value and to contunually improve supporting processes and procedures'

## design principals

- perform operations as code
- annotate documentation
- make frequent, small, reversible changes
- refine operastion precedures frequently
- antipate failure
- learn from all operation failures

## best practices

### prepare

    'drive operational excellence with effective prepration'

- standard monitoring
- cloudformation for iac
- testing failure (choas monkey)
- use aws config / cloudtrail

### operate

    'measure success with the achivement of business and customer outcomes'

- cloudwatch for monitoring
- cloudtrail to monitor infrastructure changes
- aws x-ray (monitoring containers)

### evolve

    'evolve operations to sustain opertional excellence'

- devops
  - aws devops services
    - codebuild (build and test service)
    - codecommit (git repo)
    - codedeploy (deploy)
    - codepipeline (combine codecommit, codebuild etc)
    - codestar (jira)
    - aws x-ray )optimize

[home](../README.md)