# Viewing details for high\-volume entities<a name="high-degree-entities"></a>

In the [behavior graph](behavior-graph-data-about.md), Amazon Detective tracks relationships between entities\. For example, each behavior graph tracks when an AWS user creates an AWS role and when an EC2 instance connects to an IP address\.

When an entity has too many relationships during a time period, Detective cannot store all of the relationships\. When this occurs during the current scope time, Detective notifies you\. Detective also provides a list of occurrences of high\-volume entities\.

## What is a high\-volume entity?<a name="high-degree-entity-about"></a>

During a given time interval, an entity might be the origin or destination of an extremely large number of connections\. For example, an EC2 instance may have connections from millions of IP addresses\.

Detective maintains a limit on the number of connections that it can accommodate during each time interval\. If an entity exceeds that limit, then Detective discards the connections for that time interval\.

For example, assume that the limit is 100,000,000 connections per time interval\. If an EC2 instance is connected to by more than 100,000,000 IP addresses during a time interval, then Detective discards the connections from that time interval\.

However, you might be able to analyze that activity based on the entity at the other end of the relationship\. To continue the example, while an EC2 instance might be connected to from millions of IP addresses, a single IP address connects to far fewer EC2 instances\. Each IP address profile provides details about the EC2 instances that the IP address connected to\.

## Viewing the high\-volume entity notification on a profile<a name="high-degree-entity-profile-notification"></a>

Detective displays a notice at the top of a finding or entity profile if the scope time includes a time interval where the entity is high\-volume\. For finding profiles, the notice is for the involved entity\.

The notice includes the list of relationships that have high\-volume time intervals\. Each list entry contains a description of the relationship and the start of the high\-volume time interval\.

A high\-volume time interval might be an indicator of suspicious activity\. To understand what other activity occurred at the same time, you can focus your investigation on a high\-volume time interval\. The high\-volume entity notice includes an option to set the scope time to that time interval\.

**To set the scope time to a high\-volume time interval**

1. In the high\-volume entity notice, choose the time interval\.

1. On the pop\-up menu, choose **Apply scope time**\.

## Viewing the list of high\-volume entities for the current scope time<a name="high-degree-entity-list"></a>

The **High\-volume entities** page contains a list of high\-volume time intervals and entities during the current scope time\.

**To display the High\-volume entities page**

1. Open the [Detective console](https://console.aws.amazon.com/detective/)\.

1. In the Detective navigation pane, choose **High\-volume entities**\.

Each entry in the list contains the following information:
+ The start of the high\-volume time interval
+ The identifier and type of the entity
+ The description of the relationship, such as "EC2 instance connected from IP address"

You can filter and sort the list by any of the columns\. You can also navigate to the entity profile for an involved entity\.

**To navigate to the profile for an entity**

1. In the **High\-volume entities** list, choose the row to navigate from\.

1. Choose **View profile with high\-volume scope time**\.

When you use this option to navigate to an entity profile, the scope time is set as follows:
+ The scope time starts 30 days before the high\-volume time interval\.
+ The scope time ends at the end of the high\-volume time interval\.