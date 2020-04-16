# Overview of the behavior graph data structure<a name="graph-data-structure-overview"></a>

The behavior graph data structure defines the structure of the extracted and analyzed data\. It also defines how the source data is mapped to the behavior graph\.

## Types of elements in the behavior graph data structure<a name="graph-data-structure-elements"></a>

The behavior graph data structure is made up of the following information elements\.

****Entity****  
An entity represents an item extracted from the Detective source data\.  
Each entity has a type, which identifies the type of object it represents\. Examples of entity types include IP addresses, Amazon EC2 instances, and AWS users\.  
For each entity, the source data is also used to populate entity properties\. Property values might be extracted directly from source records or aggregated across multiple records\.  
Some properties consist of a single scalar or aggregated value\. For example, for an Amazon EC2 instance, Detective tracks the type of instance and the total number of bytes processed\.  
Time series properties track activity over time\. For example, for an EC2 instance, Detective tracks over time the unique ports that it used\.

****Relationships****  
A relationship represents activity occurring between individual entities\. Relationships are also extracted from the Detective source data\.  
Similar to an entity, a relationship has a type, which identifies the types of entities involved and the direction of the connection\. An example of a relationship type is IP addresses connecting to Amazon EC2 instances\.  
For each individual relationship, such as a specific IP address connecting to a specific instance, Detective tracks the occurrences over time\.

## Types of entities in the behavior graph data structure<a name="entity-types"></a>

The behavior graph data structure consists of entity and relationship types that do the following:
+ Track the servers, IP addresses, and user agents being used
+ Track the AWS users, roles, and accounts being used
+ Track the network connections and authorizations that occur in your AWS environment

The behavior graph data structure contains the following entity types\.

**AwsAccount**  
AWS accounts that are present in the Detective source data\.  
For each account, Detective answers several questions:  
+ What API calls has the account used?
+ What user agents has the account used?
+ What autonomous system organizations \(ASOs\) has the account used?
+ In what geographic locations has the account been active?

**AwsRole**  
AWS roles that are present in the Detective source data\.  
For each role, Detective answers several questions:  
+ What API calls has the role used?
+ What user agents has the role used?
+ What ASOs has the role used?
+ In what geographic locations has the role been active?

**AwsUser**  
AWS users that are present in the Detective source data\.  
For each user, Detective answers several questions:  
+ What API calls has the user used?
+ What user agents has the user used?
+ In what geographic locations has the user been active?

**Ec2Instance**  
Amazon EC2 instances that are present in the Detective source data\.  
For Amazon EC2 instances, Detective answers several questions:  
+ What IP addresses have communicated with the instance?
+ What ports have been used to communicate with the instance?
+ What volume of data has been sent to and from the instance?
+ What VPC contains the instance?

**Finding**  
Findings uncovered by Amazon GuardDuty that are fed into the Detective source data\.  
For each finding, Detective tracks the finding type, origin, and the time window for the finding activity\.  
It also stores information specific to the finding, such as roles or IP addresses that are involved in the detected activity\.

**IpAddress**  
IP addresses that are present in the Detective source data\.  
For each IP address, Detective answers several questions:  
+ What API calls has the address used?
+ What ports has the address used?
+ What users and user agents have used the IP address?
+ In what geographic locations has the IP address been active?

**UserAgent**  
User agents that are present in the Detective source data\.  
For each user agent, Detective answers questions such as the following:  
+ What API calls has the user agent used?
+ What users and roles have used the user agent?
+ What IP addresses have used the user agent?