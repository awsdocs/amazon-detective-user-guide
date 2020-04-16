# Changing the scope time<a name="scope-time-changing"></a>

As you work through an investigation, you can adjust the scope time\. Amazon Detective uses the scope time to conduct its analysis and to display charts, timelines, and other visualizations\.

For example, if the original analysis was based on activity from a single day, you might want to expand that to a week or a month\. The expanded period could help you get a better sense of whether the activity fits a normal pattern or is indeed unusual\.

When you change the scope time, Detective repeats its analysis and updates the displayed data based on the new scope time\.

The scope time cannot be shorter than one hour nor longer than one year\. The start and end time must be on an hour\.

## Setting specific start and end dates and times<a name="scope-time-select-date"></a>

You can set the scope time start and end dates from the Detective console\.

**To set specific start and end times for the new scope time**

1. On a finding or entity profile, under **Scope time**, choose **Edit**\.

1. On the **Edit scope time** panel, under **Start**, choose the new start date and time for the scope time\. For the new start time, you choose the hour only\.

   Remember that in Detective, all times are in UTC\.

1. Under **End**, choose the new end date and time for the scope time\. For the new end time, you choose the hour only\. The end time must be at least an hour later than the start time\.

1. To set whether the scope time is locked, use **Lock**\.

1. When you're finished editing, to save the changes and update the displayed data, choose **Update scope time**\.

## Selecting a length of time from the current time<a name="scope-time-select-length"></a>

When you set a scope time length, Detective sets the scope time to that amount of time from the current time\.

**To set the scope time length**

1. From a finding or entity profile, under **Scope time**, choose **Edit**\.

1. On the **Edit scope time** panel, next to **Historical**, choose the length of time for the scope time\.

   Specifying a time range updates the **Start** and **End** settings\.

1. To set whether the scope time is locked, use **Lock**\.

1. When you're finished editing, to save the changes and update the displayed data, choose **Update scope time**\.

## Restoring the default scope time for the current profile<a name="scope-time-restore-default"></a>

For finding profiles, the default scope time reflects the first and last times the finding was observed\. For entity profiles, the default scope time is the previous 24 hours\.

**To restore the scope time to the default for the current profile**

1. On a finding or entity profile, under **Scope time**, choose **Edit**\.

1. On the **Edit scope time** panel, next to **Historical**, choose **Default**\.

1. To set whether the scope time is locked, use **Lock**\.

1. When you're finished editing, to save the changes and update the displayed data, choose **Update scope time**\.