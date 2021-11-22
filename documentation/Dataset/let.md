![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/letstatement

</p>

 **Summary:**
<p>
The let operator binds names to expressions. Let allows for users to establish variables with static values or even take on the results of a query. Let is defined before the main body of the query.
</p>

 **Example:**
<p>
let IPAddresses = SigninLogs | summarize by IPAddress; SecurityAlert | where todynamic(Entities) in IPAddresses

let EastUSDevices = datatable(name:string) [
    'dc01',
    'dc02',
    'dc03',
    'eusfw'
];
SecurityEvent | where EastUSDevices has_any(Computer)

let query1 = Table | predicate;
let query2 = Table | predicate;
query1
| join query 2 on CommonColumn
</p>

 **When to use:**
<p>
let is a fantastic way to declare a new variable that can be either static or dynamic. As shown in the example above, the variable can take on the values of another query. When performing joins, let can be set variables to take on the results from the 2 queries and then join in a more simplified workflow. 
</p>
