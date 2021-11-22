![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/betweenoperator
</p>

 **Summary:**
<p>
The between operator matches the input that is inside the inclusive range. This can be between integers or datetime items.
</p>

 **Example:**
<p>
SecurityAlert | where TimeGenerated between (now .. ago(8d)) | where ProviderName has 'm365 defender' </br>
SecurityEvent | where TimeGenerated < ago (1h)| where EventID between (4000 .. 5000) | where Computer has 'dc01' </br>
SigninLogs | where TimeGenerated between (datetime(2021-01-01 00:00:00) .. datetime(2021-02-01 00:00:00)) | where Account has 'admin' <br/>
</p>

 **When to use:**
<p>
between is a strong operator when looking for data within a time range or numerical range. For time ranges, it can return data generated between two or more months without having to compare the time to the current time. For number ranges, this can be used in place of a < > comparison for ranges.
</p>
