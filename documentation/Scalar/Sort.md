![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/sortoperator

</p>

 **Summary:**
<p>
The sort operator sorts the rows of the input table in order by one or more columns. Asc )ascending) and desc (descending) are used to dictate which sorting method is used.
</p>

 **Example:**
<p>
SecurityEvent | project TimeGenerated, Computer, User | sort by Computer asc  </br>

SigninLogs | project TimeGenerated, Account | sort by TimeGenerated asc </br>
</p>

 **When to use:**
<p>
sort is best used when looking to surface certain results first in the list. Sort can apply to any returned column in order to organize the results. 
</p>
