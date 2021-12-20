# Pivoting to an entity profile or finding overview from Amazon GuardDuty or AWS Security Hub<a name="profile-pivot-from-service"></a>

From the Amazon GuardDuty console, you can navigate to the entity profile for an entity that is related to a finding\.

From the GuardDuty and AWS Security Hub consoles, you can also navigate to a finding overview, which also provides links to the entity profiles for the involved entities\.

These links can help to streamline the investigation process\. You can quickly use Detective to see the associated entity activity and determine next steps\. You can then archive a finding if it is a false positive or explore further to determine the scope of the problem\.

## How to pivot to the Amazon Detective console<a name="profile-pivot-how-to"></a>

The investigation links are available for all GuardDuty findings\. GuardDuty also allows you to choose whether to navigate to an entity profile or to the finding overview\.

**To pivot to Detective from the GuardDuty console**

1. Open the GuardDuty console at [https://console\.aws\.amazon\.com/guardduty/](https://console.aws.amazon.com/guardduty/)\.

1. If necessary, choose **Findings** in the left navigation pane\.

1. On the GuardDuty **Findings** page, choose the finding\.

   The finding details pane displays to the right of the finding list\.

1. On the finding details pane, choose **Investigate in Detective**\.

   GuardDuty displays a list of available items to investigate in Detective\.

   The list contains both the related entities, such as IP addresses or EC2 instances, and the finding\.

1. Choose an entity or the finding\.

   The Detective console opens in a new tab\. The console opens to the entity or finding profile\.

   If you have not enabled Detective, then the console opens to a landing page that provides an overview of Detective\. From there, you can choose to enable Detective\.

**To pivot to Detective from the Security Hub console**

1. Open the AWS Security Hub console at [https://console\.aws\.amazon\.com/securityhub/](https://console.aws.amazon.com/securityhub/)\.

1. If necessary, choose **Findings** in the left navigation pane\.

1. On the Security Hub **Findings** page, choose a GuardDuty finding\.

1. In the details pane, choose **Investigate in Detective** and then choose **Investigate finding**\.

   When you choose **Investigate finding**, the Detective console opens in a new tab\. The console opens to the finding overview\.

   The Detective console always opens to the Region where the finding originated, even if you pivot from your aggregation Region\. For more information about finding aggregation, see [Aggregating findings across Regions](https://docs.aws.amazon.com/securityhub/latest/userguide/finding-aggregation.html) in the *AWS Security Hub User Guide*\.

   If you have not enabled Detective, the console opens to the Detective landing page\. From there, you can enable Detective\.

## Troubleshooting the pivot<a name="profile-pivot-troubleshooting"></a>

To use the pivot, one of the following must be true:
+ Your account must be an administrator account for both Detective and the service you are pivoting from\.
+ You have assumed a cross\-account role that grants you administrator account access to the behavior graph\.

For more information about the recommendation to align administrator accounts, see [Recommended alignment with Amazon GuardDuty and AWS Security Hub](https://docs.aws.amazon.com/detective/latest/adminguide/detective-prerequisites.html#recommended-service-alignment) in *Detective Administration Guide*\.

If the pivot does not work, check the following\.
+ **Does the finding belong to an enabled member account in your behavior graph?** If the associated account was not invited to the behavior graph as a member account, then the behavior graph does not contain data for that account\.

  If an invited member account did not accept the invitation, then the behavior graph does not contain data for that account\.
+ **Is the finding archived?** Detective does not receive archived findings from GuardDuty\.
+ **Did the finding occur before Detective began to ingest data into your behavior graph?** If the finding is not present in the data that Detective ingests, then the behavior graph does not contain data for it\.
+ **Is the finding from the correct Region?** Each behavior graph is specific to a Region\. A behavior graph does not contain data from other Regions\.