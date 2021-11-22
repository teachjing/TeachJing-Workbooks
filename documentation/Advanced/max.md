![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/max-aggfunction

</p>

 **Summary:**
<p>
The max operator returns the maximum value across a group.
</p>

 **Example:**
<p>
SecurityEvent | summarize max(TimeGenerated)  </br>
SigninLogs | summarize dcountif(tostring(Status), tostring(Status) has 'MFA') by UserDisplayName | summarize max(dcountif_Status) </br>
</p>

 **When to use:**
<p>
Max performs the same functionality as arg_max. It is best used when looking for the top value of a column or when looking for the most recent event.
</p>
