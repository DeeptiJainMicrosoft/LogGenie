# LogGenie
A standalone windows application which helps in reading Azure Monitor logs for all Azure Services archived to an Azure Storage Account. Best suited for scenarios requiring quick, lightweight log review or when minimal setup and management effort is needed.

**Purpose:**

* Simplifies the analysis of Azure Monitor diagnostic logs stored in Azure Storage Accounts.
* Organize the log containers based on Azure services.
* Include the resource name alongside the log file name.
* Reduces troubleshooting time and collaboration overhead across Azure teams.

**_Unique Scenarios:_**

Handles cases where log analytics tables are unavailable, providing an essential alternative for analyzing such logs archived to storage accounts.

**Key Features:**

* Standalone Application: Windows-based, .NET-powered tool for log analysis.
* Direct Access to Logs: Reads logs directly from Azure Blob Storage in JSON format without additional costs or management complexity.
* Supports All Azure Services: Works for logs from services like Azure Core (VM, Networking), Developer, and App Service, especially when log analytics tables are unavailable.
* Customizable Configuration: Flexible setup allows reading logs by simply adding log container names in the XML file.

**Benefits:**
* Faster Log Analysis: Offers lightweight, immediate, ad-hoc analysis of archived logs.
* Cost-Efficient: Avoids additional expenses by directly accessing storage logs.
* Enhanced Troubleshooting: Speeds up resolving issues by bypassing dependencies on storage team for log analysis.


```Ensure that key-based access is enabled for the storage account```

Containers were specified based on [Azure Monitoring resource logs](https://learn.microsoft.com/en-us/azure/azure-monitor/reference/supported-logs/microsoft-cache-redis-logs)


![Log Genie Demo](https://github.com/DeeptiJainMicrosoft/LogGenie/blob/main/LogGenie.gif)
