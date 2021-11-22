![Documentation](https://shields.io/badge/-Documentation-informational)

https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/unionoperator?pivots=azuremonitor

**Summary:**
<p>
The union operator takes two or more tables and returns the rows of them all in a stacked fashion.
</p>

**Example:**
<p>
SecurityAlert | union SecurityIncident
OfficeActivity | union workspace('workspacenumber2').OfficeActivity
SecrityBaseline | where Computer has 'dc01' | union Update where Computer has 'dc01'

</p>

**When to use:**
<p>
Union is best used when looking to combine results from two or more tables into one location. Union is also the main operator when performing cross-workspace queries.
</p>