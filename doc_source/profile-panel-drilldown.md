# Exploring activity details on a profile panel<a name="profile-panel-drilldown"></a>

After you assess that a finding might be a true positive, the next step is to dig deeper into the pattern of activity for the related resources\.

On the following profile panels, you can display a summary of the activity details:
+ **Overall API call volume**, except for the profile panel on the user agent profile
+ **Newly observed geolocations**, except for the profile panel on the federated user profile
+ **Overall VPC flow volume**
+ **VPC flow volume to and from the finding IP address**, for findings that are associated with a single IP address

The activity details can answer these types of questions:
+ Which IP addresses were used?
+ Where were those IP addresses located?
+ Which API calls did each IP address make, and from which services did they make those calls?
+ Which principals or access key identifiers \(AKIDs\) were used to make the calls?
+ What resources were used to make those calls?
+ How many calls were made? How many succeeded and failed?
+ What volume of VPC flow data was sent to or from each IP address?

**Topics**
+ [Activity details for Overall API call volume](profile-panel-drilldown-overall-api-volume.md)
+ [Activity details for a geolocation](profile-panel-drilldown-new-geolocations.md)
+ [Activity details for Overall VPC flow volume](profile-panel-drilldown-overall-vpc-volume.md)
+ [Activity details for VPC flow volume to and from the finding's IP address](profile-panel-drilldown-vpc-to-from-finding-ip.md)