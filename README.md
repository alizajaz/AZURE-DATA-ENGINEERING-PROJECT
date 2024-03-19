# AZURE-DATA-ENGINEERING-PROJECT
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
- how to mount cloud to Databricks
- Databricks 
- Pyspark for data cleaning
- Spark SQL for analysis
- POWER BI for visualization

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






