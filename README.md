DAY-1
## Introduction:
the main goal was to set up the basic cloud environment and create the ingestion layer. This prepares the system to receive banking data from different sources like ATM logs, UPI logs, and customer files.

Azure Services Required:
Azure Storage Account (ADLS Gen2) – create Container:
{“raw/transactions/ ,raw/atm/ ,raw/upi/ ,raw/customers/”}
Azure Function App:
We will create “Event Grid Trigger function”, Runtime: Python
Azure Event Grid Subscription:
Create Event Grid Subscription (Storage → Function App)
Event Grid Subscription → Blob Created → Trigger eventgrid_ingestor Function
Azure Service Bus”
Create:
•	Namespace
•	Queue: transactions-ingestion

## VS Code Commands:
•	Create a new Azure Functions project
{ func init ingestion_app –python”}
•	Create Event Grid Trigger Function
{ func new --name eventgrid_ingestor --template "EventGridTrigger"}
•	Add your connection strings
{ AzureWebJobsStorage , SERVICEBUS_CONNECTION}
•	Install required Python packages
•	Run the function locally

