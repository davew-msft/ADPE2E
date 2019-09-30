
# Azure End-to-End Big Data - One Day Event

Dave Wentzel  
Microsoft MTC Architect: Data & AI  
linkedin.com/in/dwentzel  

## Agenda 

Get Started as soon as possible:  

* `git clone https://github.com/davew-msft/ADPE2E`
* **To get everyone started quickly, begin deploying the Azure infrastructure as soon as you can.**  See [Lab Deployment](./Deploy/Deploy.md).  
  * Use `US East`, not `US East2`
  * **If you get a failure message during deployment, let me know immediately**

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

### [Lab 1: Load Data into Azure SQL Data Warehouse using Azure Data Factory Pipelines](./Lab/Lab1/Lab1.md)

This lab sets up the basic tooling needed to complete the remaining labs.  

### [Lab 2: Transform Big Data using Azure Data Factory and Azure SQL Data Warehouse](./Lab/Lab2/Lab2.md)

In this lab we will copy csv files from the NYC Taxi dataset to our local data lake and SQL Data Warehouse.  We'll use Azure Data Factory to orchestrate a pipeline to do this.  

### [Lab 3: Explore Big Data using Azure Databricks](./Lab/Lab3/Lab3.md) 

In this lab you will use Azure Databricks to explore the New York Taxi data files you saved in your data lake in Lab 2. Using a Databricks notebook you will connect to the data lake and query taxi ride details. 


### [Lab 4: Add AI to your Big Data Pipeline with Cognitive Services](./Lab/Lab4/Lab4.md)
In this lab you will use Azure Data Factory to download New York City images to your data lake. Then, as part of the same pipeline, you are going to use an Azure Databricks notebook to invoke Computer Vision Cognitive Service to generate metadata documents and save them in back in your data lake. The Azure Data Factory pipeline then finishes by saving all metadata information in a Cosmos DB collection. You will use Power BI to visualise NYC images and their AI-generated metadata.

The estimated time to complete this lab is: **60 minutes**.

Step     | Description
-------- | -----
![](./Media/Blue1.png) | Build an Azure Data Factory Pipeline to copy image files from shared Azure Storage
![](./Media/Blue2.png) | Save image files to your data lake
![](./Media/Blue3.png) | For each image in your data lake, invoke an Azure Databricks notebook that will take the image URL as parameter
![](./Media/Blue4.png) | For each image call the Azure Computer Vision Cognitive service to generate image metadata. Metadata files are saved back in your data lake
![](./Media/Blue5.png) | Copy metadata JSON documents into your Cosmos DB database
![](./Media/Blue6.png) | Visualize images and associated metadata using Power BI

### [Lab 5: Ingest and Analyse real-time data with Event Hubs and Stream Analytics](./Lab/Lab5/Lab5.md)
In this lab you will use an Azure Logic App to connect to Twitter and generate a stream of messages using the hashtag #NYC. The logic app will invoke the Azure Text Analytics Cognitive service to score Tweet sentiment and send the messages to Event Hubs. You will use Stream Analytics to generate the average Tweet sentiment in the last 60 seconds and send the results to a real-time dataset in Power BI.

The estimated time to complete this lab is: **60 minutes**.

Step     | Description
-------- | -----
![](./Media/Orange1.png) | Build an Azure Logic App to invoke the Twitter API and retrieve Tweets with the hashtag #NYC
![](./Media/Orange2.png) | For each Tweet, invoke the Azure Text Analytics Cognitive service to detect its sentiment score
![](./Media/Orange3.png) | Format and send the Tweet’s JSON message to Event Hubs
![](./Media/Orange4.png) | Save Tweet messages into your data lake for future analysis (cold path)
![](./Media/Orange5.png) | Send stream of Tweet messages to Stream Analytics for real-time analytics (hot path)
![](./Media/Orange6.png) | Visualize real-time data generated by Stream Analytics with Power BI

## Workshop Agenda

The workshop content will be delivered over the course of two days with the following agenda:

### Day 1
Activity | Duration
-------- | ---------
Workshop Overview |
Modern Data Platform Concepts: Part I |
**Modern Data Warehousing** |
Lab 1: Load Data into Azure SQL Data Warehouse using Azure Data Factory Pipelines    | 60 minutes
Modern Data Platform Concepts: Part II |
Lab 2: Transform Big Data using Azure Data Factory and Azure SQL Data Warehouse    | 45 minutes

### Day 2

Activity | Duration
-------- | ---------
**Advanced Analytics** |
Modern Data Platform Concepts: Part III |
Lab 3: Explore Big Data using Azure Databricks    | 30 minutes
Modern Data Platform Concepts: Part IV |
Lab 4: Add AI to your Big Data Pipeline with Cognitive Services    | 60 minutes
**Real-time Analytics** |
Modern Data Platform Concepts: Part V |
Lab 5: Ingest and Analyse real-time data with Event Hubs and Stream Analytics   | 60 minutes