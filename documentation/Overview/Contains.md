![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/datatypes-string-operators
</p>

 **Summary:**
<p>
The contains operator takes a string and filters the logs based on the string. Contains is not case sensitive.
</p>

 **Example:**
<p>
SecurityAlert | where ProviderName contains 'm365 defender' </br>
SecurityEvent | where EventID == 4624 | where Computer contains 'dc01' </br>
SigninLogs | where TimeGenerated < ago(1h) | where Account contains 'admin' <br/>
</p>

 **When to use:**
<p>
Contains can be used in place of the usual '==' string comparison filter while providing relaxed case sensitivity. This can be useful when performing searches and filtering of logs on an item where capitalization is unknown.
</p>
