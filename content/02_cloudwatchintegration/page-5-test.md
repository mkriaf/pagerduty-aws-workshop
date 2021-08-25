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

v2
- Navigate to the URL in the Sample Application CloudFormation output and verify it is running.
- Go to Services -> EC2 , Select the EC2 Machine that is running the webserver from the list and click "Connect"
- run the command "systemctl stop ngnix" to simulate a situation where the webserver stopped working.
- Navigate to the URL in the Cloudformation output and verify it is NOT running.
- Refresh a few times to generate errors for Cloudwatch.
- A PagerDuty Incident should be created. 
- To resolve the incident, navigate back to the shell page and run "systemctl start ngnix", to restart the webserver.
