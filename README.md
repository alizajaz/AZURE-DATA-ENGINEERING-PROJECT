# AZURE-DATA-ENGINEERING-PROJECT
Data Ingestion, Data Transformation, Data Loading and Reporting.
Complete end-to-end Azure data engineer project

- DATA Migration from on-prem SQL to Azure Cloud
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
**STEP 1 **
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
Create Storage Account
Go to the Search button in  https://portal.azure.com/#home type storage >click on storage account>click create button 
Create a storage account











