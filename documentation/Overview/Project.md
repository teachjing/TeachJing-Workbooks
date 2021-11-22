![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/projectoperator
</p>

 **Summary:**
<p>
The project operator returns only the columns specified in the query. This operator is useful when looking to trim results to only return the columns and content of value or interest. Project can also rename columns when returning them.
</p>

 **Example:**
<p>
SecurityAlert | project TimeGenerated, AlertName, ProviderName, Entities </br>
SecurityEvent | where EventID == 4624 | project Computer, User, ActionPerformed=Process </br>
SigninLogs | where TimeGenerated < ago(1h) | project Account, TimeGenerated, Result <br/>
</p>

 **When to use:**
<p>
Project should be used when lookin to eliminate unneeded columns from results. This will make the results more personalized but also will increase query performance. When renaming columns, this is useful when looking to rename columns when normalizing data or performing joins as the columns can then share a common column title if that is not already the case.
</p>
