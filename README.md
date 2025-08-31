# LogGenie
A standalone windows application which helps in reading Azure Monitor logs for all Azure Services archived to an Azure Storage Account. Best suited for scenarios requiring quick, lightweight log review or when minimal setup and management effort is needed.

**Purpose:**

* Simplifies the analysis of Azure Monitor diagnostic logs stored in Azure Storage Accounts.
* Organize the log containers based on Azure services.
* Include the resource name alongside the log file name.
* Reduces troubleshooting time and collaboration overhead across Azure teams.

**Key Features:**

* Alternative to Log Analytics: Analyze logs directly from Azure Storage when Log Analytics tables are not available.
* Standalone Application: Windows-based, .NET-powered tool for log analysis.
* Direct Access to Logs: Reads logs directly from Azure Blob Storage in JSON format without additional costs or management complexity.
* Supports All Azure Services: Works for logs from services like Azure Core (VM, Networking), Azure Storage, and App Service, especially when log analytics tables are unavailable.
* Customizable Configuration: Flexible setup allows reading logs by simply adding log container names in the XML file.

**Benefits:**
* Faster Log Analysis: Offers lightweight, immediate, ad-hoc analysis of archived logs.
* Cost-Efficient: Avoids additional expenses by directly accessing storage logs.
* Enhanced Troubleshooting: Speeds up resolving issues by bypassing dependencies on storage team for log analysis.

**Known Limitations:**
* Ensure that key-based access is enabled for the storage account.
* Enforcing different network restrictions on the storage account can impact connectivity.
* Application may fail to read very large log files (greater than 10 MB).

**The detailed step-by-step guide for using LogGenie is available at [Step-By-Step guide](https://github.com/DeeptiJainMicrosoft/LogGenie/blob/main/Step-By-Step%20guide.md), with a demo provided below for your reference.**
**     **
![Log Genie Demo](https://github.com/DeeptiJainMicrosoft/LogGenie/blob/main/LogGenie.gif)

**_Note:_** _To read Azure Monitor classic log files, you can leverage https://github.com/nunogabrielmonteiro/AzureStorageLogReader_
