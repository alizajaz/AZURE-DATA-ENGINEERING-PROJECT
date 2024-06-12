
# AZURE-DATA-ENGINEERING-PROJECT/Azure storage account/Azure data factory/integration run time/Azure data factory pipeline
Data Ingestion, Data Transformation, Data Loading and Reporting.
Complete end-to-end Azure data engineer project

Requirement
1. DATA Migration from on-prem SQL to Azure Cloud
2. Data available in SQL table, we want to store data in Azure Storage Account.
3. Create a pipeline and schedule it so the pipeline will run automatically.
   
- How to create an Azure storage account
- how to create an Azure data factory 
- how to set integration run time
- how to create an Azure data factory pipeline


*************************************************************************************************************************************************************************************************************
Step 1 
Open Azure account> I have a storage account. Under Data Storage>There is the container.> (+Container)Create one new container>open data factory studio 
Create Azure data factory using Azure portal >create a pipeline > Since data is available in SQL server we have to move to Azure.


1. Create an integration runtime

manage >integration runtimes>new>azure self hosted>self hosted >it will give you key >choose manual and download 
https://www.microsoft.com/en-us/download/details.aspx?id=39717
registered Integration runtime> Once the integration runtime is set up> create a pipeline that will help to transfer data SQL server to Azure cloud(Blob Storage).

 **2. Create a Pipeline**

pipeline(Under Factory Resources)>Copy data>drag copy data>source>new dataset >select (from where you want to extract data my is MySQL>)new linked service>enter the server name, username, password, test connection 
once you can connect successfully. create, you can see table chose table >click ok 
move to sink location(Target)
click new>Azure blob storage >linked service>pass subscription >storage account> click create> select folder (my folder name is output)>click ok >publish all>trigger>refresh you can see successful running pipeline
go to storage account > you can see output file in txt format


if you have to schedule trigger >add trigger>new edit>schedule



note:

To migrate data from an on-premises SQL database to an Azure Storage Account, start by creating an Azure Storage Account. Sign in to the Azure portal, navigate to "Storage accounts," and click "Add." Provide the necessary details such as subscription, resource group, storage account name, region, and performance options, then click "Review + create" and "Create."

Next, create an Azure Data Factory. In the Azure portal, search for "Data factories" and click "Add." Fill in the required fields including subscription, resource group, and Data Factory name, select the version, and region, then click "Review + create" and "Create." After deployment, go to the Data Factory resource.

Set up the Integration Runtime to connect to your on-premises data. In the Data Factory portal, under "Manage," select "Integration Runtimes," click "New," choose "Self-hosted" and follow the wizard to download and install the Integration Runtime on a local machine. Register the runtime and copy the authentication key.

Create a Data Factory pipeline to move the data. In the Data Factory portal, go to "Author & Monitor" and under "Author," click on "Pipelines" and then "New pipeline." Add a new copy activity. In the "Source" tab, configure the on-premises SQL database by creating a linked service using the Integration Runtime. In the "Sink" tab, configure the Azure Storage Account by creating a linked service and specifying the destination container. Set up mappings if necessary.

Finally, schedule the pipeline. Under "Triggers," click "New/Edit," and create a new trigger. Set the desired schedule, activate the trigger, and attach it to the pipeline. Save and publish all changes. The pipeline will now run automatically according to the defined schedule, transferring data from the on-premises SQL database to the Azure Storage Account.












