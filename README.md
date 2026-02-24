# Shopping Mart - Medallion Architecture using Microsoft Fabric

### Project Overview

This project demonstrates an **end-to-end data engineering solution** built using **Microsoft Fabric**, implementing the **Medallion Architecture (Bronze, Silver, Gold)**.

Implemented a retail use case (**Shopping Mart**) to process and analyze data related to **orders, customers, products and reviews**, enabling business insights through a Power BI dashboard.

---

### Architecture Overview

The architecture follows a layered approach:

**Git Source → Bronze (Raw) → Silver (Transformed) → Gold (Business Layer) → Semantic Model → Power BI Reports**

<img width="1027" height="490" alt="image" src="https://github.com/user-attachments/assets/ab9c7cb0-c686-4e26-a8f1-b9beade01ab1" />


### Key components implemented 

* Metadata-driven ingestion in Lakehoue using JSON configuration by Data pipelines
* Multi-Lakehouse architecture (Bronze, Silver, Gold)
* PySpark based transformations in Notebooks
* Shortcuts and Materialized Lake Views (MLVs) for performance optimization
* End-to-end pipeline orchestration by invoking the ingestion pipeline
* Semantic modeling for reporting
* Power BI dashboards for visualization

---

### Bronze Layer (Raw Data)

* Data ingested from Git repository
* Using metadata configuration for source and target file names and types(csv, json)
* Stored in raw format without transformations
  #### *Data Pipeline*
<img width="932" height="424" alt="image" src="https://github.com/user-attachments/assets/c0ea19a0-ded1-4058-ad51-f69868be1563" />

  #### *Bronze Lakehouse*
<img width="953" height="303" alt="image" src="https://github.com/user-attachments/assets/24620940-5aa9-4cdf-b569-b29fbd3fe49c" />

 Refer to `bronze` folder for details

---

### Silver Layer (Transformation)

* Data cleaning and transformations using PySpark and implenting Upserts
  #### *Silver Notebook*
<img width="767" height="413" alt="image" src="https://github.com/user-attachments/assets/fd6676e1-c701-45f3-b63d-c1fe656a7d44" />

<img width="709" height="401" alt="image" src="https://github.com/user-attachments/assets/4bccc9b1-2975-4942-9075-1178f720da3c" />

<img width="718" height="397" alt="image" src="https://github.com/user-attachments/assets/b7b21473-4457-4ffd-9a8b-61e683d8c2dd" />



  #### *Silver Lakehouse*
<img width="667" height="407" alt="image" src="https://github.com/user-attachments/assets/ecfe47f5-79ae-4849-a312-36dab6bf7bc5" />

 Refer to `silver` folder for notebook

---

### Gold Layer (Business Layer)

* Creating **Shortcuts** and **Materialized Lake Views (MLVs)**
* Aggregated datasets for business reporting

#### *Gold Notebook*
<img width="711" height="401" alt="image" src="https://github.com/user-attachments/assets/e2020450-1e95-42b6-80af-0f3e264f88b9" />

<img width="713" height="410" alt="image" src="https://github.com/user-attachments/assets/bb74eadc-18b7-473c-bb26-b5d073cad28d" />

#### *Gold Lakehouse*
<img width="629" height="383" alt="image" src="https://github.com/user-attachments/assets/ec0073bf-2a27-439f-9553-f21762b3b970" />

 Refer to `gold` folder for details

---
### Final Pipeline Orchestration

<img width="770" height="392" alt="image" src="https://github.com/user-attachments/assets/022d0e6d-d0dd-42c9-9ad5-2324aef00317" />

### Sementic Model
Relationships are created between the materialized views tables utilizing the direct lake mode

<img width="491" height="407" alt="image" src="https://github.com/user-attachments/assets/199adf9d-9a03-4c57-8e38-95d0ddb87f35" />


### Power BI Report
The final layer provides business insights through interactive report and drill through

<img width="673" height="403" alt="image" src="https://github.com/user-attachments/assets/1ab6e8a3-faa6-4f8f-b774-0df590e16ded" />


<img width="758" height="400" alt="image" src="https://github.com/user-attachments/assets/4daa6beb-7c26-48ef-a8c4-26ee08d9769a" />


### Workspace Lineage View
<img width="536" height="385" alt="image" src="https://github.com/user-attachments/assets/6a4a7413-95ce-4967-9081-f36bf3e33f37" />

---

### Conclusion

This project showcases a **production-style modern data platform** using Microsoft Fabric, combining data engineering, transformation, and analytics into a unified solution.
