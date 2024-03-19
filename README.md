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






****
General knowledge****
In Azure Cloud, there are many ways to import data depending upon the source of data, size of data, specific service you prefer to use, existing infrastructure, specific requirements, and preferences.

CREATE DATABASE IN My SQL WorkBench
CREATE DATABASE sales;
USE sales;

DATABASE NAME: sale
right click >Table Data Import Wizard >file path>next>next>finish(make sure to put it in (int)
or  Expand Databases, right-click a database (test in the example below), point to Tasks, and click Import Flat File above Import Data.

SELECT * FROM sale.pizza_sales;(SelectPizzasale.png)
"The data needs to be transferred to cloud storage."
Now we need to open azure cloud 
**signup Azure account First **
https://azure.microsoft.com/en-us/free/cloud-services/search/?ef_id=_k_Cj0KCQjwqdqvBhCPARIsANrmZhPaFblMgmBumsootUo-hhTKu2VrwcztAWwHpFkGJKungy3xGAR9eloaAr3TEALw_wcB_k_&OCID=AIDcmm5edswduu_SEM__k_Cj0KCQjwqdqvBhCPARIsANrmZhPaFblMgmBumsootUo-hhTKu2VrwcztAWwHpFkGJKungy3xGAR9eloaAr3TEALw_wcB_k_&gad_source=1&gclid=Cj0KCQjwqdqvBhCPARIsANrmZhPaFblMgmBumsootUo-hhTKu2VrwcztAWwHpFkGJKungy3xGAR9eloaAr3TEALw_wcB
Sign up Start Free> You can use Microsoft email to log in>next >You have to insert your card number address and every detail asked by Microsoft Azure then you will be able to log in once confirmed by Microsoft Azure. 

*****************************************************************************************************************************************************************
**Create Storage Account, Container, upload a file**
**************************************************************************************************************************************************************
There are 4 storage services>blob, file, table, and queue.
Based on requirements we used this storage service.
************************************************************************************************************************************************************************
**blob storage**>Requiremnent where data is unstructured format such as video file, audio file, txt file, doc
**File Storage**(Shared location)> E.g. many teams working together on the same project but from different locations such as Nepal, India, USA, etc. You want to share location files where everyone can access upload, and make changes.
**Table Storage** :Structure Data 
**Queue Storage** Put files in the queue and process them one by one. That kind of scenario uses Queue storage.
***********************************************************************************************************************************************************************

**Account type**
**Blob
General purpose v1
General purpose v2(Azure recommendation)**

***************************************************************************************************************************************************************************

**Access Tier**
**Hot tier:** access data frequently, we store files in the hot tier.

**Cold Tier**: Infrequently

**Archive Tier:** Rarely
***************************************************************************************************************************************************************************




Go to the Search button in  https://portal.azure.com/#home type storage >click on storage account>click create button 
Create a storage account
https://github.com/alizajaz/AZURE-DATA-ENGINEERING-PROJECT/blob/main/AzureStoragewithresourcesstoragename.png
add resources group if you do not have one>storage account name >Review+Create>deployment process will happen >click on> go to resource>you can view an overview of storage >click on container >click on +> create the container>add name and you can give access to private, public>click create  and once a container is successfully created upload a file.>click on file >upload a file >click on file name>edit>preview
https://github.com/alizajaz/AZURE-DATA-ENGINEERING-PROJECT/blob/main/Azurestoragecontainerfileupload1.png 
















