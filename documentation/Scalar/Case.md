![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/casefunction
</p>

 **Summary:**
<p>
The case operator evaluates a list of items and returns the first result when the item is satisfied. If none of the items are true, the result of the last item is returned. Case can be seen as a list of if/else statements that runs a check on each item to see if they are true. If not, return the default else value.
</p>

 **Example:**
<p>
Table | extend Variable = case( Size <= 3, "Small", Size <= 10, "Medium", "Large") </br>
SecurityEvent | extend Category = case(EventID between (4620 .. 4630), "Authentication", EventID between (4720 .. 4730), "Account based", "Unclassified") | project EventID, Category  </br>
</p>

 **When to use:**
<p>
Case should be used when looking to tag or classify data based on filters. The return value for each case can be a static string or a dyanmic value from a column/variable. This can be used to filter out only relvant columns when looking to perform case matching.
</p>
