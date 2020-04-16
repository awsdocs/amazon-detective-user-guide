# Displaying activity details for a profile panel<a name="profile-panel-drilldown"></a>

After making an initial assessment that a finding might be a true positive, the next step is to dig deeper into the activity details\.

On the following profile panels, you can display a summary of the activity details\.
+ **Overall API call volume**, except for the profile panels on the IP address profile and the user agent profile
+ **Newly observed geolocations**

The activity details are specific to a subset of the profile panel data\. For the **Overall API call volume** profile panel, the activity details are limited to a selected time interval\. For the **Newly observed geolocations** profile panel, the activity details are limited to a selected geolocation\.

The activity details can answer these types of questions:
+ Which IP addresses were used?
+ Where were those IP addresses located?
+ Which API calls did each IP address make?
+ Which access key identifiers \(AKIDs\) were used to make the calls?
+ What resources were used to make those calls?
+ How many calls were made? How many succeeded and failed?

## Displaying the activity details<a name="profile-panel-drilldown-populating"></a>

The activity details appear at the bottom of the profile panel\.

On the **Overall API call volume** profile panel, to display the activity details, choose a time interval\.

On the **Newly observed geolocations** profile panel, to display the activity details, do one of the following:
+ On the map, choose a geolocation\.
+ In the list, choose **Details** for a geolocation\.

On the **Newly observed geolocations** profile panel, the activity details replace the geolocation list\. To return to the geolocation list, choose **Return to all results**\.

## Activity details for an API call volume time interval<a name="profile-panel-drilldown-api-time-interval-content"></a>

Each tab in the activity details provides information about the same set of API calls that were issued during the selected time interval\.
+ The **Observed IP addresses** tab initially displays the list of IP addresses used to issue API calls\.

  You can expand each IP address to display the list of API calls that were issued from that IP address\.

  You can then expand each API call to display the list of AKIDs that issued that API call from that IP address\.  
![\[View of the Observed IP addresses tab of the Overall API call volume panel, with an entry expanded to show the hierarchy of IP address, API calls, and AKIDs.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_api_ipaddress.png)
+ The **API method** tab initially displays the list of API calls that were issued\.

  You can expand each API method to display the list of IP addresses from which the calls were issued\.

  You can then expand each IP address to display the list of AKIDs that issued that API call from that IP address\.  
![\[View of the API method tab of the Overall API call volume panel, with an entry expanded to show the hierarchy of API call, IP addresses, and AKIDs.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_api_apimethods.png)
+ The **Access Key ID** tab initially displays the list of AKIDs that were used to issue API calls\.

  You can expand each AKID to display the list of IP addresses from which the AKID issued API calls\.

  You can then expand each IP address to display the list of API calls that were issued from that IP address using that AKID\.  
![\[View of the Access key ID tab of the Overall API call volume panel, with an entry expanded to show the hierarchy of AKIDs, IP addresses, and API calls.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_api_akids.png)

For each entry, the activity details show the number of successful and failed calls\. The **Observed IP addresses** tab also shows the location of each IP address\.

## Activity details for a geolocation<a name="profile-panel-drilldown-geolocation-content"></a>

Each tab in the activity details provides information about the set of API calls that were issued from a geolocation during the scope time\. The API calls include all calls issued from the geolocation\. They are not limited to calls that used the finding or profile entity\.
+ The **Observed IP addresses** tab initially displays the list of IP addresses that were used to issue API calls from the selected geolocation\.

  You can expand each IP address to display the resources that issued API calls from that IP address\. The list displays the resource name\. To see the principal ID, hover over the name\.

  You can then expand each resource to display the specific API calls that were issued from that IP address by that resource\.  
![\[View of the Observed IP addresses tab of the Newly observed geolocations panel, with an entry expanded to show the hierarchy of IP address, resources, and API methods.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_geo_ips.png)
+ The **Resource** tab initially displays the list of resources that issued API calls from the selected geolocation\. The list displays the resource name\. To see the principal ID, hover over the name\. For each resource, the **Resource** tab also displays the associated AWS account\.

  You can expand each user or role to display the list of API calls that were issued by that resource\.

  You can then expand each API call to display the list of IP addresses from which the resource issued the API call\.  
![\[View of the Resource tab of the Newly observed geolocations panel, with an entry expanded to show the hierarchy of user or role, API methods, and IP addresses.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_geo_resources.png)

For each IP address, resource, and API method, the list shows the number of successful and failed API calls\.

## Sorting the activity details<a name="profile-panel-drilldown-sort"></a>

You can sort the activity details by any of the list columns\.

When you sort using the first column, only the top\-level list is sorted\. The lower level lists are always sorted by the count of successful API calls\.

## Filtering the activity details<a name="profile-panel-drilldown-filter"></a>

You can use the filtering options to focus on specific subsets or aspects of the activity represented in the activity details\.

On all of the tabs, you can filter the list by any of the values in the first column\.

**To add a filter**

1. Choose the filter box\.

1. From **Resources**, choose the property to use for the filtering\.

1. Provide the value to use for the filtering\. The filter supports partial values\. For example, if you are filtering by API method, to only include API methods that affect policies, filter by **Policy**\.

   For API methods and IP addresses, you can either specify a value or choose a built\-in filter\.

   For **Common API substrings**, choose the substring that represents the type of action, such as `List`, `Create`, or `Delete`\. Each API method name starts with the action type\.  
![\[List of built-in filtering options for API methods\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_filterapi.png)

   For **CIDR patterns**, you can choose to only include public IP addresses, private IP addresses, or IP addresses that match a specific CIDR pattern\.  
![\[List of built-in filtering options for IP addresses.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_filteripaddress.png)

1. If you have multiple filters, choose a Boolean option to set how those filters are connected\.  
![\[List of available connectors between individual filters for the activity details filter.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/screen_profile_panel_drilldown_filterconnectors.png)

1. To remove a filter, choose the x icon in the top right corner\.

1. To clear all of the filters, choose **Clear filter**\.