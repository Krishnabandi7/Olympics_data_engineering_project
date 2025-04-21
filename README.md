# Olympics_data_engineering_project

This project demonstrates an end-to-end data engineering pipeline for processing Olympics data using Azure services. It extracts data from APIs and CSV files, ingests it into Azure Data Factory, stores it in Azure Data Lake, transforms it using Databricks with Unity Catalog, and performs analytics with Azure Synapse Analytics. The transformed data is visualized in a Power BI dashboard. The pipeline is orchestrated with CI/CD using Azure DevOps.

Project Overview

The goal is to build a scalable data pipeline to process Olympics data (e.g., athlete details, events, medals) and create insightful visualizations. The pipeline leverages Azure's cloud ecosystem for data ingestion, storage, transformation, analytics, and visualization.

Architecture





Data Sources:





APIs: Olympics data from public APIs (e.g., athlete stats, event schedules).



CSV Files: Historical Olympics data stored in CSV format.



Ingestion:





Azure Data Factory (ADF): Orchestrates data extraction from APIs and CSV files. ADF pipelines pull data and store it in Azure Data Lake Storage Gen2.



Storage:





Azure Data Lake Storage Gen2: Stores raw data in a hierarchical structure for scalability and accessibility.



Transformation:





Azure Databricks: Performs data cleaning, transformation, and enrichment using PySpark. Unity Catalog is used for governance, ensuring data lineage, access control, and metadata management.



Analytics:





Azure Synapse Analytics: Runs SQL-based queries on transformed data for aggregations (e.g., medals by country, athlete performance trends). Synapse integrates with Power BI for seamless data access.



Visualization:





Power BI: Connects to Synapse Analytics to create an interactive dashboard displaying Olympics insights, such as:





Medal tallies by country.



Athlete performance over time.



Event participation trends.



CI/CD:





Azure DevOps: Automates deployment of ADF pipelines, Databricks notebooks, and Synapse SQL scripts. The CI/CD pipeline ensures consistent and repeatable deployments.

Pipeline Workflow





Data Ingestion:





ADF pipelines extract data from APIs (using HTTP connectors) and CSV files (from blob storage or local uploads).



Data is saved in raw format in the Data Lake (raw zone).



Data Transformation:





Databricks notebooks process raw data, performing tasks like:





Data cleaning (handling missing values, standardizing formats).



Joining datasets (e.g., athlete and event data).



Aggregations (e.g., medals by country or year).



Unity Catalog manages schemas, tables, and access policies.



Transformed data is saved in the curated zone of the Data Lake.



Analytics with Synapse:





Synapse Analytics runs SQL queries on curated data to generate datasets for reporting (e.g., top-performing countries, event summaries).



Serverless SQL pools enable ad-hoc querying, while dedicated SQL pools handle large-scale analytics.



Visualization in Power BI:





Power BI connects to Synapse Analytics via DirectQuery or import mode.



The dashboard includes:





Bar charts for medal counts by country.



Line charts for athlete performance trends.



Pie charts for event category distributions.



Filters for year, country, and sport.



CI/CD with Azure DevOps:





Code for ADF pipelines, Databricks notebooks, and Synapse scripts is stored in a GitHub repository.



Azure DevOps pipelines:





CI: Build and validate code changes.



CD: Deploy updates to ADF, Databricks, and Synapse environments.
