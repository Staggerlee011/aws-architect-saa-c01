# cloudwatch

- monitoring tool that can collect data about aws services as well as ec2 instances

## cloudwatch metrics

- configure cloudwatch alarms to trigger alerts based on cloud metrics (lambda, etc)
- autoscaling uses cloudwatch
- can create custom metrics (free memory on ec2) via api

- ec2 (cpu, etc using hypervisor)
- s3 (number of objects, bucket size etc)
- elb (requests, unhealthy host count)

- standard monitoring every 5 min
- detailed monitoring every 1 min

## cloudwatch logs

- based on installing agent for ec2 etc
- log streams ()
- define which logs you want to monitor with cloudwatch
- can be made into metrics for reviewing

## cloudwatch events

- example ec2 stopping, starting, creation, deletion
- trigger events based on events
- schedule events (snapshots etc)

## ec2 monitoring with cloudwatch

- system status check
  - basic monitoring (network connection, system power, hardware issue)
  - solution normally restart instance!
- instance checks
  - failed system checks
  - max memory

## cloudwatch alarms

- based on cloudwatch metrics
- can trigger event (sns, lambda)
- billing alarm
- events based notification
  - schedules
- logs ()
- metrics (list services and pre made metrics)

[home](../README.md)