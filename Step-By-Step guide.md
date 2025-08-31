## Follow the steps below to get started with LogGenie.


1. Download the Release.zip from [LogGenie GitHub Repository](https://github.com/DeeptiJainMicrosoft/LogGenie)
2. Extract the zip and run "**LogGenie.exe**" from the Release folder.
3. Click on **+** sign before Log Sink in left panel.
4. Right Click "**Storage Accounts**" and select the option to add Azure storage account.
5. Provide the Azure storage account connection string for the storage account where you are ingesting your service logs.

        Make sure that Access Key authentication is enabled on your storage account.
        
6. Once connected, expand the **+** sign. You will see your storage account name with a tree view of all Azure services ingesting logs into that account.
7. Each azure service will show a list of containers created by Azure Monitor to store logs.
8. To add a log file, right-click on a container and select "**Add Log file**".
9. A pop-up will appear prompting for the path of the log file. Copy the log file path from your storage account and paste it into the text box.

        For example: "resourceId=/SUBSCRIPTIONS/{subscription id}/RESOURCEGROUPS/{resource group name}/PROVIDERS/{service resource provider}/NETWORKSECURITYGROUPS/{resource name}/y=2024/m=09/d=25/h=09/m=00/PT1H.json"

10. Similarly, you can repeat this process to add log files in same or other containers. 
11. Once log files have been added, right-click the container and select "**Import Logs**".
12. Logs will be displayed in the right-hand window.
13. Total number of log entries can be viewed under "**Row Count**".
14. Click "**Clear Logs**" to remove loaded log data.
15. Data can be exported into Excel or CSV format using "Export to Excel" or "Export to CSV" buttons at the bottom of the right panel.
16. You can also load a previously downloaded log file using the "**Add Logs**" button.
17. Apply filters to refine the data by selecting a column from the log file and providing filter criteria.
         
         For example:
                Select "StatusCode" in the filter dropdown, enter "404" in the text box, then click Apply.

         You can also use Custom Filters for advanced queries:
                Select "Custom" in the filter dropdown, enter "StatusCode < '400' and OperationName like '%list%'" in the text box, then click Apply.


**If you don’t see logs for a specific service, it means the configuration is missing in the XML file.**
  
- You can find the container mappings for Azure services in the **LogContainersList.xml** file under the Debug and Release folders.
- To check a full list of Azure service log categories, refer to [Azure Monitor Supported Logs](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-logs/microsoft-cache-redis-logs)


**Please follow the steps below to add a New Service Log Category:**
1. Download the "**Source Code.zip**".
2. Extract the code.
3. Navigate to the path: "**\Source Code\LogGenie\LogGenie\bin\Debug**"
4. Open **LogContainersList.xml** and add a new entry in the following format:

        <LogCategory type="ServiceType" name="logcategory">insights-logs-logcategory</LogCategory>

        For example: <ServiceLogs type="Batch" name="servicelogs">insights-logs-servicelogs</ServiceLogs>
5. Rebuild the solution in both **Debug** and **Release** mode.
6. Run **LogGenie.exe** again.
