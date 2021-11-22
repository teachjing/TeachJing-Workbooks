![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/mvexpandoperator

</p>

 **Summary:**
<p>
The mv-expand operator expands a dynamic list of items into multiple records. These dynamic lists will appear as nested JSON lists that have not been seperated. The result of this call will separate the items from the lsit into individual rows.
</p>

 **Example:**
<p>
SecurityAlert | extend Entity = todynamic(Entities) | mv-expand Entity
</p>

 **When to use:**
<p>
Mv-expand is best used when looking to expand or unpack a nested or regular JSON array. This is best used when looking to utilize contents of the array for checks, joins, or calling on the content in other queries.
</p>
