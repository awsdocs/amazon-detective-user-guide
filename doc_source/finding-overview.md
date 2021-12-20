# Viewing a finding overview<a name="finding-overview"></a>

A finding is a possible instance of malicious activity or other risk that was detected by Amazon GuardDuty\. Findings are loaded into Amazon Detective so that you can use Detective to investigate the activity associated with the involved entities\.

A Detective finding overview provides detailed information about the finding\. It also displays a summary of the involved entities, with links to the associated entity profiles\.

## Scope time used for the finding overview<a name="finding-overview-scope-time"></a>

The scope time for a finding overview set to the finding time window\. The finding time window reflects the first and last time that the finding activity was observed\.

The scope time is in UTC\.

## Finding details<a name="finding-overview-finding-details"></a>

The panel at the right contains the details for the finding\. These are the details provided by GuardDuty for the finding\.

From the finding details, you can also archive the finding\. See [Archiving an Amazon GuardDuty finding](finding-update-status.md)\.

## Related entities<a name="finding-overview-entities"></a>

The finding overview contains a list of entities that are involved in the finding\. For each entity, the list provides overview information about the entity\. This information reflects the information on the entity details profile panel on the corresponding entity profile\.

You can filter the list based on entity type\. You can also filter the list based on text in the entity identifier\.

To pivot to the profile for an entity, choose **See profile**\. When you pivot to the entity profile, the following occurs:
+ The scope time is set to the finding time window\.
+ On the **Associated findings** panel for the entity, the finding is selected\. The finding details remain displayed at the right of the entity profile\.