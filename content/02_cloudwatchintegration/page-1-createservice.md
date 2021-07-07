---
title: "Create a PagerDuty Service"
chapter: true
weight: 1
---

# Create a PagerDuty Service

In order for PagerDuty to receive alerts, a Service must be created. For more detials on this process see the service documentation [here](https://support.pagerduty.com/docs/services-and-integrations#create-a-new-service).

In PagerDuty, Choose Services in the top menu, then click the blue button "+ New Service".

![Create a new service](/images/new_service.png)

Enter your new service's name. 

*Note: When naming a PagerDuty Service, the idea is to consider the overall category for the types of events that will be sent here. This is important because when a responder gets a notification for an incident, the Service name will immediately suggest why it matters and where in my infrastructure it is impacting. For example, the impact of a "Low disk space" alert might be critical or it might be trivial depending on where it is happening in your infrastructure. Seeing that it is in the service "Inventory Database" tells me which database, which application and perhaps even the SLA requirements to respond.* 

Best Practices around naming and configuring services can be found [here](https://community.pagerduty.com/forum/t/service-configuration-guide/1660).

![Create a new service](/images/new_service_1.png)

Choose the Escalation Policy which describes whom to notify when an alert is sent to this service and becomes an Incident. If you have not yet created any Escalation Policies, it is easy to choose "Generate a new Escalation Policy". This choice will create a simple, one-level policy with your name as the on-call person 24x7. 

More information on Escalation Policies can be found [here](https://support.pagerduty.com/docs/escalation-policies).

![Choose an Escalation Policy](/images/new_service_2.png)

Choose which alert grouping scheme for this service. For this exercise, it is easiest to choose "Turn Off Alert Grouping." This means that, for every incoming alert, a new Incident will be created.

PagerDuty's Event Intelligence allows customers to automatically group multiple alerts into a single Incident. They might do this based upon a field or set of fields that are the same, or if the alerts occur at or around the same time, or PagerDuty can learn which ones ought to be grouped based upon responder behavior and past activity! More on Event Intelligence can be found [here](https://support.pagerduty.com/docs/event-intelligence).

![Choose the Alert Grouping scheme](/images/new_service_3.png)

Add a CloudWatch Integration to this service. A Service integration is essentially an endpoint that another system can send alerts. Each type of alert is different and telling PagerDuty it is a CloudWatch alert allows it to understand the particular data for CloudWatch.

![Add a CloudWatch Integration](/images/new_service_4.png)

Click "Create Service" to complete the service creation workflow.

![Click the Create Service button](/images/new_service_5.png)

You will land on the Integrations subtab. To the right of the Amazon CloudWatch integration, there is an Integration Name, Key and URL. Copy the Integration URL by clicking the copy icon to the right of the URL.

![Copy the Integration URL](/images/new_service_6.png)

Now you are ready to create an SNS Topic and notification that will send alerts to PagerDuty!

{{% notice warning %}}
<p style='text-align: left;'>
The examples and sample code provided in this workshop are intended to be consumed as instructional content. These will help you understand how various AWS services can be configured to work with PagerDuty.
</p>
{{% /notice %}}