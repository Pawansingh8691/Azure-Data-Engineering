Azure Data Engineering Project - Formula1 Data Pipeline (Ergast API)
Project Overview
This project demonstrates an end-to-end Azure Data Engineering pipeline that ingests, processes, and analyzes Formula 1 racing data from the Ergast API. The solution leverages Azure Data Factory (ADF) for orchestration, Azure Databricks for data processing, and Azure Key Vault for secure credential management.

Tech Stack & Services Used
Azure Data Factory (ADF) – Orchestrates data ingestion and pipeline execution

Azure Databricks – Processes and transforms the data using PySpark

Azure Key Vault – Secures API keys and sensitive credentials

Azure Data Lake Storage (ADLS Gen2) – Stores raw and processed data

Azure SQL Database / Synapse Analytics (Optional) – Stores structured data for analysis

Power BI (Optional) – Visualizes insights from processed data

Data Source: Ergast API
The Ergast API provides historical Formula 1 race data in JSON format. This project extracts:

Race results

Driver standings

Constructor details

Lap times and pit stops

Project Workflow
Data Ingestion

ADF calls the Ergast API to fetch JSON data.

Data is stored in Azure Data Lake Storage (ADLS) in raw format.

Data Processing (ETL in Databricks)

Databricks loads raw JSON data from ADLS.

PySpark transforms and cleanses the data.

Processed data is stored in Parquet format in ADLS.

Data Storage & Analysis

The transformed data is loaded into Azure SQL Database or Synapse Analytics for further analysis.

Power BI (optional) is used for visualization and reporting.

Security & Key Management

Azure Key Vault securely stores API keys and credentials.

ADF and Databricks fetch secrets from Key Vault instead of hardcoding them.

Setup & Deployment
Prerequisites
An Azure Subscription

Azure Data Factory, Databricks, ADLS, and Key Vault configured

Python & PySpark installed for local testing

Configure Azure Services

Create Data Factory pipelines and link them to Databricks.

Set up ADLS containers for raw and processed data storage.

Run the ADF Pipeline

Trigger the ADF pipeline to fetch data from Ergast API (or local storage).

Execute Databricks Notebook

Open Databricks and run the ETL PySpark notebook to transform data.

Load Data into SQL Database (Optional)

Store structured data in Azure SQL Database / Synapse Analytics.

Visualize in Power BI (Optional)

Connect Power BI to the SQL Database for reporting.

Future Enhancements
✅ Automate the pipeline using Azure Data Factory triggers
✅ Implement incremental data ingestion
✅ Add real-time data streaming with Event Hubs
✅ Enhance visualizations using Power BI dashboards
