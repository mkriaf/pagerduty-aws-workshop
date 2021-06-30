---
title: "Create Cloudwatch Alarm"
chapter: true
weight: 4
---

# Create Cloudwatch Alarm

In AWS, navigate to Cloudwatch.

Create a new Alarm

- The metric we want to get is the “unhealthy host count”
- This is under ApplicationELB -> Per AppELB, Per TG Metrics
- make sure that you select the correct LB name and Target Group.
- hint, if the graph is empty (non zero) it's probably the wrong LB.

Set the SNS Topic to the one we just created


{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}