![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/datatableoperator?pivots=azuremonitor

</p>

 **Summary:**
<p>
The datatable operator takes a configuration in as input and returns a table based on the configuration. The configuration consists the name of the column and the format of the data that the column will contain.
</p>

 **Example:**
<p>
datatable (Date:datetime, Event:string) [datetime(1910-06-11), "Born", datetime(1930-01-01), "Enters Ecole Navale", datetime(1953-01-01), "Published first book", datetime(1997-06-25), "Died"]
</p>

 **When to use:**
<p>
Datatable is best used when looking to construct a static table of information that can be used to run comparisions, checks, or joins within a regular log based query. 
</p>
