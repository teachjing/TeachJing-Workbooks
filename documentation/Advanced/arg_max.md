![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/arg-max-aggfunction

</p>

 **Summary:**
<p>
The arg_max operator finds a row in a group that maximizes a specified expresison and returns the value of the expression to return.</br>
</p>
Example: summarize [(NameExprToMaximize , NameExprToReturn [, ...] )=] arg_max (ExprToMaximize, | ExprToReturn [, ...])

ExprToMaximize: Expression that will be used for aggregation calculation.</br>
ExprToReturn: Expression that will be used for returning the value when ExprToMaximize is maximum. Expression to return may be a wildcard () to return all columns of the input table. </br>
</p>

 **Example:**
<p>
SecurityEvent | summarize arg_max(Computer, EventID)  </br>

SigninLogs | summarize arg_max(TimeGenerated, UserDisplayName) </br>
</p>

 **When to use:**
<p>
arg_max is best used when looking to return the highest or most recent log for a specified item. The most common use for this operator is to find the most recent log ingested from a source. This can be useful when running connector health checks, resoruce reporting health checks, and finding most recent activity on entities or events.
</p>
