# Searching for a finding or entity<a name="detective-search"></a>

With the Amazon Detective search function, you can navigate directly to the profile for a finding or entity based on its identifier\.

These are the identifiers to use for each entity type\.
+ For AWS accounts, the account ID\.
+ For IP addresses, the address\.
+ For AWS roles and AWS users, the principal ID\.
+ For user agents, the user agent name\.
+ For an Amazon EC2 instance, the instance identifier\.

Once you have the identifier, you can complete the search\.

For findings, the finding type must be one that Detective supports\. See [Supported finding types](supported-finding-types.md)\.

**To search for a finding or entity**

1. Sign in to the AWS Management Console, then open the Detective console at [https://console\.aws\.amazon\.com/detective/](https://console.aws.amazon.com/detective/)\.

1. In the navigation pane, choose **Search**\.

1. From the **Select type** menu, choose the type of item you are looking for\.

   **Examples from your data** contains a sample set of identifiers of the selected type that are in your behavior graph data\. To display the profile for one of the examples, choose its identifier\.

1. In the search field, enter the identifier to search for\.

1. Choose **Search** or press Enter\.

If Detective does not find the finding or entity, first check that you entered the correct identifier\. If the identifier is correct, you can also check the following\.
+ **Does the finding or entity belong to an enabled member account in your behavior graph?** If the associated account was not invited to the behavior graph as a member account, then the behavior graph does not contain data for that account\.

  If an invited member account did not accept the invitation, then the behavior graph does not contain data for that account\.
+ **For a finding, does Detective support that finding type?** If the finding type is not one of the types listed in [Supported finding types](supported-finding-types.md), then the behavior graph does not contain data for it\.
+ **Did the finding or entity occur before Detective began to ingest data into your behavior graph?** If the finding or entity is not present in the data that Detective ingests, then the behavior graph does not contain data for it\.
+ **Is the finding or entity from the correct Region?** Each behavior graph is specific to a Region\. A behavior graph does not contain data from other Regions\.