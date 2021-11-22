![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/summarizeoperator
</p>

 **Summary:**
<p>
The summarize operator is used to aggregate the content of a table based on the listed column or columns. This is most useful when looking to cut down on the results shown while summarizing the columns of interest. Summarize can be used by itself or with other aggregaters such as count(), arg_max(), arg_min(), or avg(). Using multiple columns allows for stronger combinations within the results.
</p>

 **Example:**
<p>
SecurityAlert | summarize count() by ProviderName | where count_ < 100 </br>
SecurityEvent | summarize by Computer, EventID </br>
SigninLogs | where TimeGenerated < ago(1h) | summarize by Account <br/>
</p>

 **When to use:**
<p>
Summarize should be used when aggregating data within logs based on relation or interest. For example, summarizing which events are reporting for device. Summarize can also be used for time-series analysis by generating the count of events by topic over a specified time range.
</p>
