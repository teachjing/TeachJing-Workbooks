![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/arg-min-aggfunction

</p>

 **Summary:**
<p>
The arg_min operator finds a row in a group that minimizes a specified expresison and returns the value of the expression to return. </br>
Example: summarize [(NameExprToMinimize , NameExprToReturn [, ...] )=] arg_min (ExprToMinimize, | ExprToReturn [, ...])
</p>
ExprToMinimize: Expression that will be used for aggregation calculation. </br>
ExprToReturn: Expression that will be used for returning the value when ExprToMinimize is minimum. Expression to return may be a wildcard () to return all columns of the input table. 
</p>

 **Example:**
<p>
SecurityEvent | summarize arg_min(Computer, EventID)  </br>

SigninLogs | summarize arg_min(TimeGenerated, UserDisplayName) </br>
</p>

 **When to use:**
<p>
arg_min is best used when looking to return the highest or most recent log for a specified item. The most common use for this operator is to find the most recent log ingested from a source. This can be useful when running connector health checks, resoruce reporting health checks, and finding most recent activity on entities or events.
</p>
