![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/datatypes-string-operators
</p>

 **Summary:**
<p>
Similar to the contains operator, the has operator takes a string and filters the logs based on the string. Contains is not case sensitive.
</p>

 **Example:**
<p>
SecurityAlert | where ProviderName has 'm365 defender' </br>
SecurityEvent | where EventID == 4624 | where Computer has 'dc01' </br>
SigninLogs | where TimeGenerated < ago(1h) | where Account has 'admin' <br/>
</p>

 **When to use:**
<p>
Has performs the same functionality as Contains but provides better performance when running the query.
</p>
