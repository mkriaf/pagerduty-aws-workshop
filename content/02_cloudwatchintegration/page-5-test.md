---
title: "Trigger an Incident"
chapter: true
weight: 6
---

## Trigger an Incident

- Navigate to the URL in the Sample Application CloudFormation output and verify it is running.
- Stop the EC2 instance.
- Navigate to the URL in the Cloudformation output and verify it is NOT running.
- Refresh a few times to generate errors for Cloudwatch.
- A PagerDuty Incident should be created. 
- Resolve the Incident
- Restart the EC2 instance.

