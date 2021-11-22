![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/min-aggfunction

</p>

 **Summary:**
<p>
The min operator returns the minumum value across a group.
</p>

 **Example:**
<p>
SecurityEvent | summarize min(TimeGenerated)  </br>

SigninLogs | summarize dcountif(tostring(Status), tostring(Status) has 'MFA') by UserDisplayName | summarize min(dcountif_Status) </br>
</p>

 **When to use:**
<p>
Min performs the same functionality as arg_min. It is best used when looking for the lowest value of a column or when looking for the oldest event.
</p>
