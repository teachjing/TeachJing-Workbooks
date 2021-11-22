![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/externaldata-operator?pivots=azuremonitor
</p>

 **Summary:**
<p>
The externaldata operator allows for queries to refernce data that is stored outside of the workspace. The most common use case for this operator is to call on data that is being stored within an Azure Storage Account blob. API endpoints or website files can also be called from within the query.

Externaldata requires that a user tells the query the structure of the data that will be brought in as well as the column names. That would appear as so: (Firstcolumn: int, Secondcolumn: string, Thirdcolumn: real). When pulling data from a blob, a SAS token will need to be generated in order for the query to access the data.
</p>

 **Example:**
<p>
let ExternalTable = externaldata(Device: string, Version: real, User: string) [@'STORAGE BLOB SAS TOKEN"] with (format=json); ExternalTable

let ExternalTable = externaldata(DisplayName:string, Version:string, Group:string) [@'https://sample.website/samplefile.csv'] with (format=csv); ExternalTable
</p>

 **When to use:**
<p>
Externaldata is a convenient way to call data from external sources in order to be usable in log format. This allows for data to be stored elsewhere while still being brought in without ingestion costs.
</p>
