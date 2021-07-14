# Activity details for VPC flow volume to and from the finding's IP address<a name="profile-panel-drilldown-vpc-to-from-finding-ip"></a>

For a finding that involves a single IP address and an EC2 instance, the activity details for **VPC flow volume to and from the finding's IP address** show the interactions between the finding EC2 instance and the finding IP address during a selected time range\.
+ To display the activity details for a single time interval, choose the time interval on the chart\.
+ To display the activity details for the current scope time, choose display details for scope time\.

If the finding is associated with multiple IP addresses, then the profile panel does not provide activity details\.

## Content of the activity details<a name="drilldown-vpc-to-from-ip-content"></a>

The content reflects the activity during the selected time range\.

The activity details contain an entry for each unique combination of local port, remote port, protocol, and direction\.

Each entry displays the volume of inbound traffic, the volume of outbound traffic, and whether the access request was accepted or rejected\.

![\[Initial view of the activity details for VPC flow volume to and from the finding's IP address\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_vpc_flow_to_from_ip_initial.png)

## Sorting the activity details<a name="drilldown-vpc-to-from-ip-sort"></a>

You can sort the activity details by any of the columns in the table\.

By default, the activity details are sorted by the inbound traffic\.

## Filtering the activity details<a name="drilldown-vpc-to-from-ip-filter"></a>

To focus on specific activity, you can filter the activity details by the following values:
+ Local or remote port
+ Direction
+ Protocol
+ Whether the request was accepted or rejected

**To add and remove filters**

1. Choose the filter box\.

1. From **Properties**, choose the property to use for the filtering\.

1. Provide the value to use for the filtering\. The filter supports partial values\.

1. If you have multiple filters, choose a Boolean option to set how those filters are connected\.  
![\[Filtering field on the activity details for VPC flow volume to and from the finding's IP address\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_vpc_flow_to_from_ip_filter.png)

1. To remove a filter, choose the x icon in the top\-right corner\.

1. To clear all of the filters, choose **Clear filter**\.

## Selecting the time range for the activity details<a name="drilldown-vpc-to-from-ip-time-range"></a>

When you first display the activity details, the time range is either the scope time or a selected time interval\. You can change the time range for the activity details\.

**To change the time range for the activity details**

1. Choose **Edit**\.

1. On **Edit time window**, choose the start and end time to use\.

1. To set the time window to the default scope time for the profile, choose **Set to default scope time**\.

1. Choose **Update time window**\.

The time range for the activity details is highlighted on the profile panel charts\.

## Displaying the volume of traffic for selected rows<a name="drilldown-vpc-to-from-ip-chart-details"></a>

When you identify rows that are of interest, you can display on the main charts the volume of traffic over time for those rows\.

For each row to add to the charts, select the check box\. For each selected row, the volume is displayed as a line on the inbound or outbound charts\.

![\[VPC flow volume to and from the finding's IP address with volume displayed for a selected row\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_vpc_flow_to_from_ip_chart_selected.png)

To focus on the traffic volume for the selected entries, you can hide the overall volume\. To show or hide the overall traffic volume, toggle **Overall traffic**\.

![\[VPC flow volume to and from the finding's IP address with overall traffic hidden\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_vpc_flow_to_from_ip_overall_off.png)