
# 🚀Azure AdventureWorks Enterprise Data Platform (ADF | ADLS Gen2 | Databricks | Synapse | Power BI)

## 📌 Project Overview
This project demonstrates a real-world, end-to-end Data Engineering solution on Microsoft Azure, following industry best practices such as Medallion Architecture (Bronze, Silver, Gold), metadata-driven pipelines, and cloud-native analytics.

✔ Ingests raw data from a **GitHub source API**

✔ Orchestrates dynamic pipelines using **Azure Data Factory (ADF)**

✔ Stores raw, transformed, and curated data in **Azure Data Lake Storage Gen2**

✔ Cleans and transforms data using **Azure Databricks (Spark)**

✔ Serves analytics-ready data via **Azure Synapse Analytics**

✔ Can be connected to **Power BI** for visualization

## 🏗️ Architecture

<img width="501" height="243" alt="architecture" src="https://github.com/user-attachments/assets/599f5ff9-2b03-4e3e-8502-74c9124dd1e9" />

## 🛠️ Technologies Used

| Category                 | Tools                                           |
| ------------------------ | ----------------------------------------------- |
| Cloud Platform           | Microsoft Azure                                 |
| Orchestration            | Azure Data Factory (ADF)                        |
| Storage                  | Azure Data Lake Storage Gen2                    |
| Big Data Processing      | Azure Databricks (Apache Spark)                 |
| Data Warehouse / Serving | Azure Synapse Analytics (Serverless SQL)        |
| Visualization            | Power BI                                        |
| Identity & Security      | Microsoft Entra ID (Azure AD), Managed Identity |
| Source System            | GitHub REST API                                 |


## 📐 Architecture Explanation

**1️⃣ Data Ingestion (ADF – Orchestration Layer)**

  - Azure Data Factory dynamically pulls multiple CSV files from GitHub
  
  - Uses Lookup + ForEach + Copy Activity
  
  - Metadata-driven ingestion using a JSON control file
  
  - Raw data is landed into Bronze layer (Data Lake)

    <img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/7afa9759-3941-40a9-861d-ec169e30b749" />




**2️⃣ Bronze Layer (Raw Data)**

  - Stores data exactly as received
  
  - No transformation, no schema enforcement
  
  - Acts as immutable raw data source

  <img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/4975bc07-b6b6-441b-9029-8c435f24e65d" />



  **3️⃣ Silver Layer (Transformation – Databricks)**

   - Azure Databricks reads Bronze data
     
   - Cleans, standardizes, and formats data
   
   - Converts data to Parquet/Delta

   - Writes transformed output to Silver layer  


   <img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/acbfd0a1-2964-46e6-92dc-4b8087b7c412" />

----   

   <img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/b44fba6d-7395-458a-87fe-b66547ee908e" />



**4️⃣ Gold Layer (Serving – Synapse)**
  
   - Azure Synapse Serverless SQL reads Silver data
     
   - Creates schemas, views, and external tables
   
   - Data is optimized for analytics and reporting
   
   - Gold layer data is BI-ready

   <img width="940" height="440" alt="image" src="https://github.com/user-attachments/assets/6cd26d1d-6762-4e25-aea2-7734ac47b9a7" />

---

   <img width="940" height="342" alt="image" src="https://github.com/user-attachments/assets/7591294e-7c92-4121-824a-d2d9102a1bbc" />

---

  <img width="1900" height="830" alt="image" src="https://github.com/user-attachments/assets/36699934-9ada-4402-a33d-b40bec5e04f0" />

 **5️⃣ Visualization (Power BI)**

   - Power BI connects to Synapse Serverless SQL endpoint
     
   - Acts as the functional "Grand Finale" to verify that the pipeline is complete and the data is accurate.


  <img width="1525" height="983" alt="image" src="https://github.com/user-attachments/assets/cbd4a580-c6b7-472b-922e-b6158a830e10" />


---

**🎯 Key Skills Demonstrated**

   - Azure Data Factory orchestration

   - Metadata-driven pipelines

   - Azure Data Lake Gen2 design

   - Spark-based transformations (Databricks)

   - Serverless analytics with Synapse

   - End-to-end data engineering lifecycle

   - Real-world enterprise architecture

   ---

## ✅ Conclusion

This project implements a **scalable end-to-end Azure data platform** that converts raw data into **analytics-ready insights**. Using modern Azure services and Medallion Architecture, it improves data reliability, scalability, and time-to-insight, enabling faster, data-driven business decisions.


     
    






