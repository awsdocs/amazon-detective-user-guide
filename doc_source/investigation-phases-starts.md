# Investigation phases and starting points<a name="investigation-phases-starts"></a>

Amazon Detective provides tools to support the overall investigation process\. An investigation in Detective can start from a finding or an entity\. 

## Investigation phases<a name="how-detective-enables-investigation.title"></a>

Any investigation process involves the following phases:

****Triage****  
The investigation process starts when you are notified about a suspected instance of malicious or high\-risk activity\. For example, you are assigned to look into findings or alerts uncovered by services such as Amazon GuardDuty\.  
In the triage phase, you determine whether you believe the activity is a true positive \(genuine malicious activity\) or false positive \(not malicious or high\-risk activity\)\. Detective profiles support the triage process by providing insight into the activity for the involved entity\.  
For true positive instances, you continues to the next phase\.

****Scoping****  
During the scoping phase, analysts determine the extent of the malicious or high\-risk activity and the underlying cause\.  
Scoping answers the following types of questions:  
+ What systems and users were compromised?
+ Where did the attack originate?
+ How long has the attack been going on?
+ Is there other related activity to uncover? For example, if an attacker is extracting data from your system, how did they obtain it?
Detective visualizations can help you to identify other entities that were involved or affected\.

**Response**  
The final step is to respond to the attack in order to stop the attack, minimize the damage, and prevent a similar attack from happening again\.

## Starting points for a Detective investigation<a name="investigation-starting-points"></a>

Every investigation in Detective has an essential starting point\. For example, you might be assigned an Amazon GuardDuty finding to investigate\. Or you might have a concern about unusual activity tied to a specific IP address\.

Typical starting points for an investigation include findings detected by GuardDuty and entities extracted from Detective source data\.

### Findings detected by GuardDuty<a name="investigation-findings-detected"></a>

This is the most common starting point for an investigation process in Detective\. GuardDuty uses your log data to uncover suspected instances of malicious or high\-risk activity\. Detective provides resources that help you dig further into these findings\.

Starting with a finding, you can do the following:
+ See what entities, such as IP addresses and AWS accounts, are connected to that finding\.
+ See what other findings might be related to that finding\.
+ See what activity occurred close in time or location to that finding\.

For more information, see [Analyzing finding details](finding-profiles.md)\.

### Entities extracted from Detective source data<a name="investigation-entity-extracted"></a>

From the ingested Detective source data, Detective extracts entities such as IP addresses and AWS users\. You can use one of these as an investigation starting point\. For more information, see [Analyzing entity details](entity-profiles.md)\.

Detective provides general details about the entity, such as the IP address or user name\. It also provides details on activity history\. For example, Detective can report what other IP addresses an entity has connected to, been connected to, or used\.