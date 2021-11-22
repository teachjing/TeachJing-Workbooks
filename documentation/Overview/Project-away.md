![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/projectawayoperator
</p>

 **Summary:**
<p>
The project-away operator does a similar function as project. Project-away removes the unwanted columns from the full list of columns in the results.
</p>

 **Example:**
<p>
SecurityAlert | project-away ProcessingEndTime, Type </br>
SecurityEvent | where EventID == 4624 | project-away SourceComputerID, MG, MandatoryLabel </br>
SigninLogs | where TimeGenerated < ago(1h) | project-away Level, ProcessingTimeInMilliseconds <br/>
</p>

 **When to use:**
<p>
Project-away is best used when most columns should remain except for a select few. It is easier to use project-away to remove the few columns rather than using project to recreate the list of columns to present in the results.
</p>
