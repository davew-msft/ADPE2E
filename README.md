
# Azure End-to-End Big Data - One Day Event

Dave Wentzel  
Microsoft MTC Architect: Data & AI  
linkedin.com/in/dwentzel  

## Agenda 

Get Started as soon as possible:  

* `git clone https://github.com/davew-msft/AzDataPlat`
* **To get everyone started quickly, begin deploying the Azure infrastructure as soon as you can.**  See [Lab Deployment](./Deploy/Deploy.md).  
  * Use `US East`, not `US East2`
  * **If you get a failure message during deployment, let me know immediately**
* A presentation that covers the background of the Azure Data Services covered today can be found [here](Slides/Azure Data Platform End2End.pptx).  

## Background

In this workshop you will learn the main concepts related to advanced analytics and Big Data processing and how Azure Data Services can be used to implement a modern data warehouse architecture. You will understand what Azure services you can leverage to establish a solid data platform to quickly ingest, process and visualise data from a large variety of data sources. The reference architecture you will build as part of this exercise has been proven to give you the flexibility and scalability to grow and handle large volumes of data and keep an optimal level of performance.

In the exercises in this lab you will build data pipelines using data related to New York City. The workshop was designed to progressively implement an extended modern data platform architecture starting from a traditional relational data pipeline. Then we introduce big data scenarios with large files and distributed computing. We add non-structured data and AI into the mix and finish with real-time streaming analytics. You will have done all of that by the end of the day.

![](./Media/ModernDataPlatformReferenceArchitecture.jpg)

## Data Source References
New York City data used in this lab was obtained from the [New York City Open Data website](https://opendata.cityofnewyork.us/). The following datasets were used:

* [NYPD Motor Vehicle Collisions](https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions/h9gi-nx95)
* [TLC Yellow Taxi Trip Data](https://www1.nyc.gov/site/tlc/about/tlc-trip-record-data.page)

## Lab Prerequisites and Deployment
The following prerequisites must be completed before you start these labs:

* You must have an Azure account with administrator- or contributor-level access to your subscription. If you don’t have an account, you can sign up for free following the instructions here: https://azure.microsoft.com/en-au/free/
* Lab 5 requires you to have a Twitter account. If you don’t have an account you can sign up for free following the instructions here: https://twitter.com/signup. 
* Lab 5 requires you to have a Power BI Pro account. If you don’t have an account you can sign up for a 60-day trial for free here: https://powerbi.microsoft.com/en-us/power-bi-pro/

## Lab Guide

Throughout a series of 5 labs you will progressively implement the modern data platform architecture referenced below:

![](./Media/LabArchitecture.jpg)

### [Lab Deployment](./Deploy/Deploy.md)

This sets up the base infra and services in Azure.  

### [Lab 1: Load Data into Azure SQL Data Warehouse using Azure Data Factory Pipelines](./Lab/Lab1/Lab1.md)

This lab sets up the basic tooling needed to complete the remaining labs.  

### [Lab 2: Transform Big Data using Azure Data Factory and Azure SQL Data Warehouse](./Lab/Lab2/Lab2.md)

In this lab we will copy csv files from the NYC Taxi dataset to our local data lake and SQL Data Warehouse.  We'll use Azure Data Factory to orchestrate a pipeline to do this.  *This lab requires completion of the previous labs.*

### [Lab 3: Explore Big Data using Azure Databricks](./Lab/Lab3/Lab3.md) 

In this lab you will use Azure Databricks to explore the New York Taxi data files you saved in your data lake in Lab 2. Using a Databricks notebook you will connect to the data lake and query taxi ride details. *This lab requires completion of the previous labs.*


### [Lab 4: Add AI to your Big Data Pipeline with Cognitive Services](./Lab/Lab4/Lab4.md)

In this lab we will analyze NYC image data using:  
* our data lake
* our ADF pipelines
* pre-baked AI solutions called Cognitive Services that run in an Azure Databricks notebook.  

We will save the data back to our data lake for later analytics.  We'll also save metadata about our images to a NoSQL database.  We'll also use Power BI to visualize our data and metadata.  

### [Lab 5: Ingest and Analyse real-time data with Event Hubs and Stream Analytics](./Lab/Lab5/Lab5.md)

In this lab we'll ingest and analyze Twitter data using the #NYC hashtag.  We'll use another Cognitive Service (pre-built AI solution) to tell us the sentiment of the tweet.  All of this will be done in real-time using a Power BI data set.  


## Workshop Shared Resources

This is our data vendor's storage account:
    <br>- **Name**: NYCTaxiDataVendor
    <br>- **SAS URL**: 
    ```
    https://mdwresources.blob.core.windows.net/?sv=2018-03-28&ss=b&srt=sco&sp=rwl&se=2050-12-30T17:25:52Z&st=2019-04-05T09:25:52Z&spr=https&sig=4qrD8NmhaSmRFu2gKja67ayohfIDEQH3LdVMa2Utykc%3D


Alternatively, use `davewdemodblobs` in `davew demo` subscription.  