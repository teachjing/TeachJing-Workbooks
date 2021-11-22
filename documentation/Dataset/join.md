![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
 https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/joinoperator?pivots=azuremonitor

</p>

 **Summary:**
<p>
The join operator mergres the rows of two tables to form a new table by matching the specified values.

There are several types of joins:

kind=leftanti, kind=leftsemi The result table contains columns from the left side only.

kind=rightanti, kind=rightsemi The result table contains columns from the right side only.

kind=innerunique, kind=inner, kind=leftouter, kind=rightouter, kind=fullouter A column for every column in each of the two tables, including the matching keys. The columns of the right side will be automatically renamed if there are name clashes.
</p>

 **Example:**
<p>
SigninLogs | where UserDisplayName has 'johndo@contoso.com' | join OfficeActivity | where UserId has 'johndo@contoso.com'

SecurityAlert | where isnotempty(SystemAlertId) | extend AlertId = tostring(SystemAlertId) | join kind=inner (SecurityIncident | where isnotempty(AlertIds) | mv-expand AlertIds | extend AlertId = tostring(AlertIds)) on AlertId | extend entity = Entities | mv-expand todynamic(['entity'])
</p>

 **When to use:**
<p>
Join is best used when looking to join columns and data from multiple tables that can provide deeper insight into events. Joins can lead to deeper detections and hunting when pulling in relevant logs.
</p>
