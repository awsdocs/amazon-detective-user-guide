# Pivoting from a profile panel to another entity or finding profile<a name="profile-panel-pivot"></a>

When a profile panel contains an identifier of a different finding or entity, it is usually a link to that finding or entity profile\. The exceptions are the links to the Amazon EC2 and IAM consoles on the EC2 instance, AWS user, and AWS role profiles\. See [Pivoting from a profile panel to another console](profile-panel-console-links.md)\.

For example, from a list of IP addresses, you might be able to display the profile for a specific IP address\. That way you can see if there is any other information available to help you to complete your investigation\.

The scope time used on the profile you pivot to is based on whether the scope time is locked\.
+ If the scope time is locked, then the profile you pivot to uses the same scope time as the profile you pivot from\.
+ If the scope time is not locked, then the profile you pivot to uses the default scope time for the profile\.

See [Locking or unlocking the scope time](scope-time-lock-unlock.md)\.