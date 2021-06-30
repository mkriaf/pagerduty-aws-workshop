---
title: "Test"
chapter: true
weight: 5
---

# Test

- Navigate to the URL in the Cloudformation output and verify it is running.
- Stop the EC2 instance.
- Navigate to the URL in the Cloudformation output and verify it is NOT running.
- Refresh a few times to generate errors for Cloudwatch.
- A PagerDuty Incident should be created. 
- Resolve the Incident
- Restart the EC2 instance.


{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}