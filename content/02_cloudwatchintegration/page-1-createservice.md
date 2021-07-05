---
title: "Create a PagerDuty Service"
chapter: true
weight: 1
---

# Create a PagerDuty Service

In order to PagerDuty to receive alerts, a Service must be created. For more detials on this process see the service documentation [here](https://support.pagerduty.com/docs/services-and-integrations#create-a-new-service).

In PagerDuty, Choose Services in the top menu, then click the blue button "+ New Service".

![Create a new service](/images/new_service.png)

Enter your new service's name. 

*Note: When naming a PagerDuty Service, we must consider the overall category for the types of events that will be sent here. This is important because when a responder gets a notification for an incident, the Service name will immediately suggest why it matters. For example, an alert from the service "Inventory Database" tells me which database, which application and perhaps even the SLA requirements to respond.* 

Best Practices around naming and configuring services can be found [here](https://community.pagerduty.com/forum/t/service-configuration-guide/1660).

![Create a new service](/images/new_service_1.png)

Choose the Escalation Policy which describes who to notify when an alert is sent to this service and becomes an Incident. If you have not yet created any Escalation Policies, it is simple to choose "Generate a new Escalation Policy". 

![Choose an Escalation Policy](/images/new_service_2.png)

Choose which alert grouping scheme for this service. For this exercise, it is easiest to choose "Turn Off Alert Grouping."

![Choose the Alert Grouping scheme](/images/new_service_3.png)

Add a CloudwWatch Integration to this service. 

![Add a CloudWatch Integration](/images/new_service_4.png)

Click "Create Service" to complete the service creation workflow.

![Add a CloudWatch Integration](/images/new_service_5.png)

You will land on the Integrations subtab. To the right of the Amazon CloudWatch integration, there is an Integration Name, Key and URL. Copy the Integration URL by clicking the copy icon to the right of the URL.

![Add a CloudWatch Integration](/images/new_service_6.png)

Now you are ready to create an SNS Topic and notification that will send to PagerDuty!

{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}