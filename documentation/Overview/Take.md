[![Goto Documentation](https://shields.io/badge/-Documentation-informational)](https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/takeoperator)

****Summary:****

The take operator returns the number of specified rows. The results are taken at random unless the rows have been sorted prior to the take operator being called.

****Example:****

SecurityAlert | take 5 <br>
SigninLogs | take 10

****When to use:****

Take is great to use when grabbing sample size results from queries. By lowering the return of rows from a query, queries perform quicker when needing a log reference.
