---
title: "Create an Event Rule"
chapter: true
weight: 4
---

# Create an Event Rule

In this section we are going to walkthrough how we to setup Rules, for our Amazon event Bridge connection between our AWS account and our PagerDuty account.

We start in our AWS console, on the Amazon Event Bridge page.
(Services → Amazon Event Bridge).

From the left hand side under ”Event” we click on “Rules”

![](/images/ebrules_1.png)

From the drop down under “Select event bus” we choose the Event Bus we created in the last section.

And click ”Create rule”.

![](/images/ebrules_2.png)


We start by giving our rule a name and a description.

![](/images/ebrules_3.png)

Next we define the pattern of event that will trigger this rule.

In our case, we have only one type of event that comes from our PagerDuty account that we want to associate with our rule.

So we select “Pre-defined pattern by service”
Then “Service Partners”.
And Finally “PagerDuty”.

Next, scroll down to “Select Targets”.

![](/images/ebrules_4.png)

Here we define the action that we want to trigger from PagerDuty, and the target/targets for that.

We can select we from various action from EC2 API Calls to Lambda Invocations.

In our demo, we are going to trigger a reboot. For that we select “ Ec2 Rebootinstaces API Call”,
Input our target Instance ID, 
And create a new role for this trigger. Then scroll down and click “Create”

![](/images/ebrules_5.png)

Back on the rules page we will see our newly created rule.

![](/images/ebrules_6.png)


{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}