---
title: "What is it?"
chapter: true
weight: 1
---

# What is this Quickstart?

### What is the PagerDuty EventBridge Quickstart?

This Quick Start deploys Amazon EventBridge integration with PagerDuty response plays on the Amazon Web Services (AWS) Cloud. PagerDuty [response plays](https://support.pagerduty.com/docs/response-automation) are packages of incident actions you can apply during an incident's lifecycle.

In this deployment, a software as a service (SaaS) event bus receives event notifications from PagerDuty and delivers them to Amazon EventBridge. An EventBridge rule evaluates incidents and invokes an AWS Step Functions workflow. The Step Functions workflow calls a Lambda function that runs the appropriate PagerDuty response play based on the incident's priority level.

![](/images/quickstart_diagram.png)

{{% notice info %}}

Complete instructions for use outside this Workshop are available [here](https://aws.amazon.com/quickstart/eventbridge/pagerduty-response-play/).

{{% /notice %}}