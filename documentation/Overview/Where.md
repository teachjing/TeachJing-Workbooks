[![Documentation](https://shields.io/badge/-Goto_Documentation-informational)]( https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/whereoperator)

**Summary:**
<p>
The where operator is the most commonly used operator within KQL. The where operator is used within almost every Kusto query. The where operator is used for filtering results based on specified criteria. This operator can be used with many other operators, such as equality operators, string operators, time based operators, and more.
</p>

**Example:**
<p>
SecurityAlert | summarize count() by ProviderName | where count_ < 100 </br>
SecurityEvent | where Computer contains 'desktop' </br>
SigninLogs | where TimeGenerated < ago(1h) <br/>
</p>

**When to use:**
<p>
Where should be used when looking to apply filtering criteria. Where is the simplest form for filtering and as mentioned can be grouped with other operators to further improve the log results.
</p>
