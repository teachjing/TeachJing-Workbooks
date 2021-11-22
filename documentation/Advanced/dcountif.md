![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/dcountif-aggfunction

</p>

**Summary:**
<p>
The dcountif operator returns an estimate of the number of distinct values of expression of rows for which the body evaluates to true.
</p>

**Example:**
<p>
SecurityEvent | summarize dcountif(EventID, tostring(EventID) startswith '46') by Computer  <br>

SigninLogs | summarize dcountif(tostring(Status), tostring(Status) has 'MFA') by UserDisplayName <br>
</p>

**When to use:**
<p>
dcountif performs the same functions and provides the same value as dcount while providing additional filtering abilities. Dcountif is best used when looking to find the count of unique values while applying filters. Using the sample scenario from dcount, dcountif would allow for the count of logins outside of the expected location to exclude the expected results.
</p>
