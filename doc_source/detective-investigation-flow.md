# Amazon Detective investigation flow<a name="detective-investigation-flow"></a>

You can use Amazon Detective to investigate an entity such as an EC2 instance or an AWS user\. You can also investigate security findings\.

At a high level, the following image shows the process for a Detective investigation\.

![\[Diagram that shows the Detective investigation process.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/diagram_investigation_flow_entity.png)

**Step 1: Select the entity to investigate**  
When looking at a finding in GuardDuty, analysts can choose to investigate an associated entity in Detective\. See [Pivoting to an entity profile or finding overview from Amazon GuardDuty or AWS Security Hub](profile-pivot-from-service.md)\.  
You can also use the Detective **Summary** page to identify an entity to investigate\. See [Using the Summary page to identify an entity of interest](summary-page.md)\.  
From a Detective finding overview, you can choose an involved entity to investigate\. See [Viewing a finding overview](finding-overview.md)\.  
You can use the Detective search function to find and select an entity to investigate\. See [Searching for a finding or entity](detective-search.md)\.  
Selecting the entity takes you to the entity profile in Detective\.

**Step 2: Analyze visualizations on profiles**  
Each entity profile contains a set of visualizations that are generated from the behavior graph\. The behavior graph is created from the log files and other data that are fed into Detective\.  
The visualizations show activity that is related to an entity\. You use these visualizations to answer questions to determine whether the entity activity is unusual\. See [Analyzing entity details](entity-profiles.md)\.  
To help guide the investigation, you can use the Detective guidance provided for each visualization\. The guidance outlines the displayed information, suggests questions for you to ask, and proposes next steps based on the answers\. See [Using profile panel guidance during an investigation](profile-panel-guidance.md)\.  
Each profile contains a list of associated findings\. You can view the details for a finding, and view the finding overview\. See [Viewing details for associated findings](entity-finding-list.md)\.  
From an entity profile, you can pivot to other entity and finding profiles, to investigate further into activity for related assets\.

**Step 3: Take action**  
Based on the results of your investigation, take the appropriate action\.  
For a finding that is a false positive, you can archive the finding\. From Detective, you can archive GuardDuty findings\. See [Archiving an Amazon GuardDuty finding](finding-update-status.md)\.  
Otherwise, you take the appropriate action to address the vulnerability and mitigate damage\. For example, you might need to update the configuration of a resource\.