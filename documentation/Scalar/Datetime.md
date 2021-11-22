![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/scalar-data-types/datetime
</p>

 **Summary:**
<p>
The datetime operator represents an instant in time, typically expressed as a date and time of day. Values range in 00:00:00 (midnight) through 11:59:59 PM.
</p>

 **Example:**
<p>
SecurityEvent | where TimeGenerated between (datetime(2021-01-01 01:45:00)..datetime(2021-01-31 11:00:00))  </br>
</p>

 **When to use:**
<p>
Datetime should be used when using the between operator or when creating a datatable. Datetime will help the query render a date that is a string and specify if a column is a date.
</p>
