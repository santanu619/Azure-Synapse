# Azure-Synapse
Azure Synapse Analytics services is one of the latest innovations from Microsoft in the Big Data and Analytics space. This service is a greatly enhanced successor of the SQL DW product. What are the main features of Azure Synapse Analytics and how is it different from SQL Data Warehousing?

A typical modern data warehouse is based on two data storage layers:
- Data Lakes - Data Lakes are designed to store unlimited data volumes, coming in different formats. This data can be structured (CSV, parquet, etc.), semi-structured (JSON, XML, etc.) or unstructured (audio/video files, text files, etc.). Data Lakes offer a low-cost storage solution, where we can store any data without worrying about its processing needs.
- Data Warehouses - Data Warehouses contain processed and structured data, ready to be consumed by business applications and reports.

Today's organizations face the following challenges, when building modern data warehouses:
- There is a need for scalable data warehousing solutions, capable of processing large amounts of data.
- Different data formats require a variety of processing and visualization tools, like SQL, Spark, Python, Power BI, etc.
- Different IT teams (like data engineers, analysts, data scientists) often work in a silo, without having visibility to each other's data and processes.
- Security teams need multiple tools to secure/audit data and manage permissions.
- Data residing in Data Lakes requires knowledge and cataloging of its schema, to explore and process.

Azure Synapse Analytics is designed to overcome many of these challenges.

## Overview of the Azure Synapse Analytics
Azure Synapse Analytics is a platform as a service, designed to unite analytics, data integration and visualization experiences for users. It has the following main features, some of them are still in a preview:
- Analytics - As a successor of SQL DW technology, Azure Synapse Analytics has inherited its Massively Parallel Processing (MPP) capability, which allows storing and efficiently processing petabytes of data, using multi-node clusters. Microsoft constantly adds new features to the SQL core engine, like workload management, materialized views, data masking, etc., which makes this product even more attractive.
- Data Exploration - A newly introduced Synapse Studio (currently in preview) makes data exploration in Data Lakes, SQL engine and Spark very easy. Users now can easily browse data in SQL and Spark tables, as well as in the Data Lakes, without knowing its schema.
- Data Integration - The Synapse Studio has inherited Azure Data Factory's data movement and transformation components, which allows building complex ETL pipelines, without a single line of code.
- Development - Azure Synapse Analytic now supports languages and platforms, like Spark, Python, Scala, as well as Spark notebooks, in addition to the traditional SQL based scripts. The users can work on data engineering, analytics, and data science tasks collaboratively, using a single tool.
- Data Visualization - Using the Synapse Studio users can connect to Power BI workspace and get the same report development experience.

## Create Azure Synapse Workspace
Most of the exciting features I mentioned above require Azure Synapse Workspace and Synapse Studio, both are currently in preview.
Let me first clarify the term pool, which we will be using as part of the Synapse Workspace. The Synapse pool represents a database within your workspace. Here are some pool types available in Synapse:
- SQL on demand - This is a serverless service, allowing you to do light data explorations in Data Lake. It is provisioned automatically when creating a workspace and users have no control over it.
- SQL pool - This is a Synapse database, based on a multi-node cluster, which is also formerly known as SQL DW database. This component is optional and may or may not exist, depending on your Data Warehouse design.
- Spark pool - This is a Spark database, based on a multi-node cluster. This is also an optional component.

It is worth mentioning that every Synapse Workspace requires at least one Data Lake account associated with it, which is specified during its creation.

## Overview of Azure Synapse Analytics
If we’re familiar with Azure SQL Data Warehouse, we already know the core features of Synapse Analytics. For example, Synapse offers cloud-based, relational data warehousing services, massively parallel processing (MPP) scale-out technology, and enough computational power to efficiently manage petabytes and petabytes of data (just like SQL Data Warehouse).
In addition to these SQL Data Warehouse features, Synapse Analytics adds new capabilities like: 
- The capability to ingest, save, query, and process non-relational data
- More integrations with Microsoft technologies
- Business intelligence integrations
- Machine learning integrations
- More efficient ingestion, transformation, management, and processing of large volume data

It’s also important to note that Azure Synapse Analytics can operate via the “on-demand serverless” model (which allows us to scale up or down and pay for only what we need when we need it), or it can operate on pre-provisioned server resources -- whichever is better for our budget and use-case.

As for operational components, Synapse consists of four fundamental parts:
1. SQL analytics: Synapse offers T-SQL analysis of our relational and non-relational data via SQL Cluster (where we pay by the computational unit) and SQL on-demand (where we pay by the number of processed terabytes). 
2. Apache Spark: Apache Spark is the leading platform for managing SQL queries, batch processing, stream processing, and machine learning analysis on large data stores.
3. Synapse Analytics Studio: Synapse Analytics Studio offers a unified workspace where we can use all of our analytics tools related to AI, ML, IoT, and BI in a single place.
4. Connectors for ingesting/integrating data from data sources: Synapse features 85 native connectors for integrating the most popular data sources so we can quickly ingest all of our data from diverse systems into the data warehouse.

### Cloud Data Warehousing, Machine Learning Analytics, and Business Intelligence
Through its deep integrations with a wide range of Microsoft Azure technologies, Azure Synapse offers cloud data warehousing, machine learning analytics, and dashboarding in a single workspace. This allows us to quickly ingest all of our data, transform and query it with SQL, analyze the data with advanced machine learning algorithms, and visualize it with Microsoft Power BI.
 
### Ingest and Query Both Structured and Unstructured Data
Azure Synapse ingests all types of data, including relational (data warehouse) data and non-relational (data lake) data, and it lets us explore this data with SQL. In this way, Synapse brings all of our structured and unstructured data (LOB, CRM, Graph, Image, Social, IoT, etc.) under the same roof for easy access and analysis. 
### Azure Data Lake Storage Gen2
Azure Synapse uses Azure Data Lake Storage Gen2 (ADLS Gen2) as a next-level data storage solution to support large-volume data analytics. ADLS Gen2 combines ADLS Gen1 features (like file-level security, scaling and file system semantics) with Azure Blob Storage features such as tiered storage, disaster recovery, and high-availability.
### Massively Parallel Processing (MPP)
Azure Synapse uses massively parallel processing (MPP) database technology, which allows it to manage analytical workloads and aggregate and process large volumes of data efficiently. In contrast to transactional databases, which store rows in a table as an object, MPP databases store each column as an object. MPP databases also distribute data across many nodes that operate in parallel to process different portions of queries. This database architecture facilitates complex, long-running analytical processes. 
### Cloud-Native Hybrid Transaction/Analytical Processing (HTAP) Implementation
Azure Synapse Analytics uses “Synapse Link” and HTAP implementation technology to achieve real-time data integrations with the Azure databases that make up our operational database infrastructure. The result is real-time machine learning and business intelligence insights drawn from live, operational data – without impacting our operational systems.
### On-Demand Serverless or Provisioned Processing Resources
Synapse gives us the ability to query massive data stores using either an on-demand serverless deployment (which scales automatically as needed to handle any processing or load) or provisioned resources. This allows organizations to either pay for what they need when they need it, or they can have a set amount of pre-provisioned processing and storage capabilities.
### Programming Language Compatibility
Azure Synapse is compatible with the widest range of scripting languages – including Scala, Python, .Net, Java, R, SQL, T-SQL, and Spark SQL. Synapse’s compatibility with so many different languages makes it suitable for a wide range of analytics tasks and data engineering profiles.
### Easy Integrations with Microsoft Technology
As a Microsoft Azure product, Synapse integrates natively with our favorite Microsoft and Azure solutions such as Azure Blob Storage, Azure Data Lake, Azure Active Directory, Azure Machine Learning, and Power BI.
### Open Data Initiative Compatibility
Azure Synapse readily integrates with solutions that adhere to the Open Data Initiative, which promotes easier data integration and compatibility between Adobe, Microsoft, and SAP technologies. Open Data Initiative solutions include products like Microsoft Dynamics 365, Microsoft Office, and Adobe Customer Experience Platform.
### Workload Optimization and Management Features
Synapse facilitates query performance tuning and optimization via limitless concurrency, workload isolation, and workload management. An example of how this works in terms of workload management could involve giving greater importance to queries from important users, like the CEO. In the following illustration, the CEO’s query gets automatically promoted from “queued” status to “running.” 
### Security and Privacy
Synapse includes the latest security and privacy technology such as real-time data masking, dynamic data masking, always-on encryption, Azure Active Directory authentication, single-sign-on authentication, and automated threat detection. The platform also allows us to control access to sensitive data via column-level and row-level security.

#### Synapse task
##### Prerequisite
- Data Lake Storage Gen 2
- Azure SQL Database
- Azure Synapse Analytics

In data lake storage, we will create a new container and giving the name as global. And, then we will create a new database and inside that a table called course. 
After that, inside of a synapse analytics account, and we will create a first pipeline to connect the SQL Database into the data lake where the data inside the table will be stored inside the data lake storage in the form of csv file and then we will call a pipeline 2 to convert that into a json format and a pipeline 3 to store that data into the database and then we will integrate all this to a master pipeline.

**Queries for creating SQL Table:-**
CREATE TABLE COURSES(CID INT,CNAME VARCHAR(50),CSTARTDATE DATE)
 
INSERT INTO COURSES VALUES(1,'AZURE','2020-10-26'),
(2,'DATABRICKS','2020-12-01'),
(3,'AWS','2021-02-01'),
(4,'Python','2021-04-01'),
(5,'sql','2021-06-01')
