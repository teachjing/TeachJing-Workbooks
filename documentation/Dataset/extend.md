![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/extendoperator

</p>

 **Summary:**
<p>
The Extend operator creates a variable and column within the body of the query. The variable created can take on the value of another column or take on a static value. Extend is also used for iff, case, and other operators.
</p>

 **Example:**
<p>
SecurityAlert | extend isSentinel = iff(ProviderName has 'asi', 'Yes', 'No') | project AlertName, isSentinel

SecurityAlert | extend Entity = todynamic(Entities) | mv-expand Entity

</p>

 **When to use:**
<p>
Extend allows for the creation of variables from within the body of the query. Variables can take on the value of other items within the logs or a static value that is deinfed by the user. It is best to use extend when looking to call upon variables or manipulate values that need to be retained.
</p>
