# Viewing details for associated findings<a name="entity-finding-list"></a>

Each entity profile contains an associated findings panel that lists the findings that involved the entity during the current scope time\. One indication that an entity has been compromised is its involvement in multiple findings\. The types of findings can also provide insight into the type of activity to be concerned about\.

The associated findings panel is displayed immediately below the entity details profile panel\.

For each finding, the table includes the following information:
+ The finding title, which is also a link to the finding overview\.
+ The AWS account associated with the finding, which is also a link to the account profile
+ The finding type
+ The earliest time that the finding was observed
+ The most recent time that the finding was observed
+ The finding severity

To display the finding details for a finding, choose the radio button for the finding\. Detective populates the finding details panel at the right of the page\. Detective also changes the scope time to be the finding time window\. This allows you to focus on activity that occurred during that time\.

If you navigated to the entity profile from a finding overview, then that finding is selected automatically and the details for the finding are displayed\.

From the finding details, to navigate back to the finding overview, choose **See all related entities**\.

You can also archive the finding\. See [Archiving an Amazon GuardDuty finding](finding-update-status.md)\.