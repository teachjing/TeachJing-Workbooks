![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/agofunction
</p>

 **Summary:**
<p>
The ago operator takes the current time and subtracts the specified amount of time from it. The time subtracted can be done in seconds (s), minutes (m), hours (h), and days (d).

ago should be used after using equality operators such as >, <, >=, <=.
</p>

 **Example:**
<p>
SecurityAlert | where TimeGenerated >= ago(2d) | where ProviderName has 'm365 defender' </br>
SecurityEvent | where TimeGenerated < ago (1h)| where EventID == 4624 | where Computer has 'dc01' </br>
SigninLogs | where TimeGenerated <= ago(30m) | where Account has 'admin' <br/>
</p>

 **When to use:**
<p>
ago should always be used when looking to filter data to be within a certain time window. >= or <= should be used when looking to return data outside of or within the time range.
</p>
