# Using the Summary page to identify an entity of interest<a name="summary-page"></a>

The Amazon Detective **Summary** page helps you to identify entities that are associated with specific types of unusual activity\. It is one of several possible starting points for an investigation\.

To display the **Summary** page, in the Detective navigation pane, choose **Summary**\. The **Summary** page is also displayed by default when you first open the Detective console\.

From the **Summary** page, you can identify entities that meet the following criteria:
+ Entities involved in activity that occurred in newly observed geolocations
+ Entities that made the largest number of API calls
+ EC2 instances that had the largest volume of traffic

From each **Summary** page panel, you can pivot to the profile for a selected entity\.

## Newly observed geolocations in the past 24 hours<a name="summary-new-geolocations"></a>

**Newly observed geolocations in the past 24 hours** highlights geographic locations that were the origin of activity during the previous 24 hours, but that were not seen during the baseline time period before that\. 

The panel includes up to 100 geolocations\. The locations are marked on the map and listed in the table below the map\.

For each geolocation, the table displays the number of failed and successful API calls made from that geolocation during the previous 24 hours\.

You can expand each geolocation to display the list of users and roles that made API calls from that geolocation\. For each principal, the table lists the type and the associated AWS account\.

If you identify a user or role that seems suspicious, then you can pivot directly from the panel to the user or role profile to continue your investigation\. To pivot to a profile, choose the user or role identifier\.

## Roles and users with the most API call volume in the past 24 hours<a name="summary-principal-api-call-volume"></a>

**Roles and users with the most API call volume in the past 24 hours** identifies the users and roles that have made the largest number of API calls during the previous 24 hours\. 

The panel can include up to 100 users and roles\. For each user or role, you can see the type \(user or role\) and the associated account\. You can also see the number of API calls issued by that user or role during the previous 24 hours\.

There is also a timeline of the API call volume for the previous seven days\. The timeline can help you to determine whether the volume of API calls is unusual for that principal\.

If you identify a user or role for which the API call volume seems suspicious, then you can pivot directly from the panel to the user or role profile to continue your investigation\. You can also pivot to the profile of the account associated with the user or role\. To pivot to a profile, choose the user, role, or account identifier\.

## EC2 instances with the most traffic volume in the past 24 hours<a name="summary-ec2-instance-traffic"></a>

**EC2 instances with the most traffic volume in the past 24 hours** identifies the EC2 instances that have had the largest total volume of traffic during the previous 24 hours\. 

The panel can include up to 100 EC2 instances\. For each EC2 instance, you can see the associated account and the number of inbound bytes, outbound bytes, and total bytes from the previous 24 hours\.

You can also see a timeline showing the inbound and outbound traffic over the previous seven days\. The timeline can help determine whether the volume of traffic is unusual for that EC2 instance\.

If you identify an EC2 instance for which the traffic volume seems suspicious, then you can pivot directly from the panel to the EC2 instance profile to continue your investigation\. You can also pivot to the profile of the account that owns the EC2 instance\. To pivot to a profile, choose the EC2 instance or account identifier\.

## Approximate value notification<a name="summary-approximate-values"></a>

On **Roles and users with the most API call volume in the past 24 hours** and **EC2 instances with the most traffic volume in the past 24 hours**, if a value is followed by an asterisk \(\*\), it means that the value is an approximation\. The true value is either equal to or greater than the displayed value\.

This occurs because of the method that Detective uses to calculate the volume for each time interval\. On the **Summary** page, the time interval is an hour\.

For each hour, Detective calculates the total volume for the 1,000 users, roles, or EC2 instances with the largest volume\. It excludes the data for the remaining users, roles, or EC2 instances\.

If a resource was sometimes in the top 1,000 and sometimes not, then the calculated volume for that resource might not include all of the data\. The data for the time intervals where it was not in the top 1,000 is excluded\.

Note that this only applies to the **Summary** page\. The profile for the user, role, or EC2 instance provides precise details\.