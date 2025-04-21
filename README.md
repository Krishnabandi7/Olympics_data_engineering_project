# Olympics_data_engineering_project

This project demonstrates an end-to-end data engineering pipeline for processing Olympics data using Azure services. It extracts data from APIs and CSV files, ingests it into Azure Data Factory, stores it in Azure Data Lake, transforms it using Databricks with Unity Catalog, and performs analytics with Azure Synapse Analytics. The transformed data is visualized in a Power BI dashboard. The pipeline is orchestrated with CI/CD using Azure DevOps.

# Project Overview

The goal is to build a scalable data pipeline to process Olympics data (e.g., athlete details, events, medals) and create insightful visualizations. The pipeline leverages Azure's cloud ecosystem for data ingestion, storage, transformation, analytics, and visualization.


# Architecture



![Flowchart (2)](https://github.com/user-attachments/assets/f005e12c-899a-40f9-b14b-07bc134f3e2d)


# Data Sources:





APIs: Olympics data from public APIs (e.g., athlete stats, event schedules).



CSV Files: Historical Olympics data stored in CSV format.



# Ingestion:





 Azure Data Factory (ADF): Orchestrates data extraction from APIs and CSV files. ADF pipelines pull data and store it in Azure Data Lake Storage Gen2.

![Screenshot 2025-04-19 190600](https://github.com/user-attachments/assets/823190bd-14a8-4f3b-8fe2-7778fd9ec5f0)

![Screenshot 2025-04-19 190545](https://github.com/user-attachments/assets/0a2a1f83-512b-4740-9d2e-97f26f64e776)

# Storage:





Azure Data Lake Storage Gen2: Stores raw data in a hierarchical structure for scalability and accessibility.

![Screenshot 2025-04-19 190412](https://github.com/user-attachments/assets/a8c8c315-afa9-412a-b403-99eedd9f23a5)


# Transformation:





Azure Databricks: Performs data cleaning, transformation, and enrichment using PySpark. Unity Catalog is used for governance, ensuring data lineage, access control, and metadata management.

![Screenshot 2025-04-19 190040](https://github.com/user-attachments/assets/9b08a3ee-4c19-4807-bcd7-5fd44d179250)
![Screenshot 2025-04-19 190725](https://github.com/user-attachments/assets/cebf78f7-2024-4ad3-a154-fc54653b8a13)

![image](https://github.com/user-attachments/assets/f5c472c2-38f4-4650-80f8-f183cc389ea2)


# Analytics:





Azure Synapse Analytics: Runs SQL-based queries on transformed data for aggregations (e.g., medals by country, athlete performance trends). Synapse integrates with Power BI for seamless data access.



# Visualization:





Power BI: Connects to Synapse Analytics to create an interactive dashboard displaying Olympics insights:


![gifdashboard](https://github.com/user-attachments/assets/b2b9fe4c-36e1-4ddc-9547-1a3d15717dbb)






CI/CD:


![Screenshot 2025-04-19 190856](https://github.com/user-attachments/assets/e0ac961f-e8c7-4a21-890f-520733df7c2f)



Azure DevOps: Automates deployment of ADF pipelines, Databricks notebooks, and Synapse SQL scripts. The CI/CD pipeline ensures consistent and repeatable deployments.






CI: Build and validate code changes.



CD: Deploy updates to ADF, Databricks, and Synapse environments.
