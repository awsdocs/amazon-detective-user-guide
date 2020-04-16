# Managing the scope time used on finding and entity profiles<a name="scope-time-managing"></a>

The charts, timelines, and other data displayed on finding and entity profiles are all based on the current scope time, which appears at the top right of each profile\. The data displayed on those charts, timelines, and other visualizations is based on the scope time\. For some profile panels, additional time is added before and after the scope time to provide context\. All times are displayed in UTC\.

Detective analytics use the scope time when checking for unusual activity\. The analytics process gets the activity during the scope time, then compares it to the activity during the 45 days before the scope time\. It also uses that 45\-day timeframe to generate baselines of activity\. 

You can always change the scope time\. You can add time to expand the view, remove time to narrow the focus, or shift the scope time earlier or later\. See [Changing the scope time](scope-time-changing.md)\.

By default, the scope time is unlocked\. As you navigate to a different profile, Detective sets the scope time to the default time window for that profile\. You can also lock the scope time, which keeps the same scope time in place as you navigate to other profiles\. See [Locking or unlocking the scope time](scope-time-lock-unlock.md)\.

**Topics**
+ [Changing the scope time](scope-time-changing.md)
+ [Locking or unlocking the scope time](scope-time-lock-unlock.md)