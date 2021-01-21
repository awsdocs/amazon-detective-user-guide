# Investigation flows in Amazon Detective<a name="detective-investigation-flow"></a>

You can use Amazon Detective to investigate a security finding or an entity such as an EC2 instance or an AWS user\.

## Overview of a typical Detective finding investigation flow<a name="investigation-flow-overview"></a>

At a high level, the following image shows the process for investigating a finding in Detective\.

![\[Diagram showing the overall flow of using Detective to triage a finding.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/diagram_investigation_flow.png)

**Step 1: Select a finding to investigate**  
When you look at a finding in Amazon GuardDuty or AWS Security Hub, you can choose to investigate the finding in Detective\. See [Pivoting to a profile from Amazon GuardDuty or AWS Security Hub](profile-pivot-from-service.md)\.  
From within Detective, you can use the Detective search function to find and select a finding to triage\. See [Searching for a finding or entity](detective-search.md)\.  
Selecting the finding takes you to the finding profile in Detective\.

**Step 2: Analyze visualizations on profiles**  
The finding profile contains a set of visualizations that are generated from the behavior graph\. The behavior graph is created from the log files and other data that are fed into Detective\.  
Most of the visualizations show activity that is related to the entity or entities involved in the finding\. You use these visualizations to answer questions that are critical to completing the triage of the finding\. See [Analyzing finding details](finding-profiles.md)\.  
To help guide the triage, you can use the Detective guidance provided for each visualization\. The guidance outlines the displayed information, suggests questions for you to ask, and proposes next steps based on the answers\. See [Using profile panel guidance during an investigation](profile-panel-guidance.md)\.  
From the finding profile, you can pivot to entity profiles to delve deeper into a specific asset that is involved with the finding\. See [Analyzing entity details](entity-profiles.md)\.

**Step 3: Update the finding status**  
Once you determine whether a finding is a true or false positive, you update the finding status in the original service\. For GuardDuty findings, Detective provides an option to archive the finding\. See [Archiving an Amazon GuardDuty finding](finding-update-status.md)\.

## Overview of a typical Detective entity investigation flow<a name="investigation-entity-flow-overview"></a>

At a high level, the following image shows the process for investigating an entity in Detective\.

![\[Diagram that shows the Detective investigation process for an entity.\]](http://docs.aws.amazon.com/detective/latest/userguide/images/diagram_investigation_flow_entity.png)

**Step 1: Select the entity to investigate**  
When looking at a finding in GuardDuty, analysts can choose to investigate an associated entity in Detective\. See [Pivoting to a profile from Amazon GuardDuty or AWS Security Hub](profile-pivot-from-service.md)\.  
You can use the Detective search function to find and select an entity to investigate\. See [Searching for a finding or entity](detective-search.md)\.  
You can also use the Detective **Summary** page to identify an entity to investigate\. See [Using the Summary page to identify an entity of interest](summary-page.md)\.  
Selecting the entity takes you to the entity profile in Detective\.

**Step 2: Analyze visualizations on profiles**  
Each entity profile contains a set of visualizations that are generated from the behavior graph\. The behavior graph is created from the log files and other data that are fed into Detective\.  
The visualizations show activity that is related to an entity\. You use these visualizations to answer questions to determine whether the entity activity is unusual\. See [Analyzing entity details](entity-profiles.md)\.  
To help guide the investigation, you can use the Detective guidance provided for each visualization\. The guidance outlines the displayed information, suggests questions for you to ask, and proposes next steps based on the answers\. See [Using profile panel guidance during an investigation](profile-panel-guidance.md)\.  
From an entity profile, you can pivot to other entity and finding profiles, to delve deeper into activity for related assets\.