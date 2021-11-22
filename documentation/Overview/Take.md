<![endif]-->

![Documentation](https://shields.io/badge/-Documentation-informational)

<p>

https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/takeoperator

</p>

****Summary:****

<p>

The take operator returns the number of specified rows. The results are taken at random unless the rows have been sorted prior to the take operator being called.

</p>

****Example:****

<p>
SecurityAlert | take 5 <br>
SigninLogs | take 10
</p>

****When to use:****

<p>
Take is great to use when grabbing sample size results from queries. By lowering the return of rows from a query, queries perform quicker when needing a log reference.
</p>
