![Documentation](https://shields.io/badge/-Documentation-informational)
<p>
https://docs.microsoft.com/en-us/azure/data-explorer/kusto/query/ifffunction
</p>

 **Summary:**
<p>
The iff operator evaluates the first argument and returns the value of either the second or last argument depending on which item is true. If true, the second option is returned. If false, the third option is returned. Iff must be used with the extend operator to create a variable that will take on the value returned from the iff statement.
</p>

 **Example:**
<p>
SecurityIncident | extend iff(isempty(Owner) == true, "This incident is not owned.", Owner)  </br>

SigninLogs | extend BrowserCheck = iff(DeviceDetail.browser !has 'Edge', "User is breaking policy by using unsupported web browsers.", "Browser compliant for this authentication.")  </br>
</p>

 **When to use:**
<p>
iff is best used when looking to set boolean checks or run checks that will leverage results desired if true or if false. Iff is a great replacement for case when looking to perform short checks rather than several.
</p>
