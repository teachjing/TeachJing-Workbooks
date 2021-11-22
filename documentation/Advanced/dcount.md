![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/dcount-aggfunction

</p>

 **Summary:**
<p>
The dcount operator returns an estimate for the number of distinct values that are taken by a scalar expression in a summary group.
</p>

 **Example:**
<p>
SecurityEvent | summarize dcount(EventID) by Computer  </br>

SigninLogs | summarize dcount(tostring(Status)) by UserDisplayName) </br>
</p>

 **When to use:**
<p>
dcount is best used when looking to summarize or estimate how many unique values exist for specified items. This can be useful for running comparisons to baselines or known values in order to determine deviations. An example would be running a count of unique values for user login methods to see if any accounts are authenticating from more than one state or country. If yes, this may show that something anomalous is has taken place.
</p>
