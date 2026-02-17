# 🛒 Shopping Mart - End-to-End Medallion Architecture using Microsoft Fabric

## 📌 Project Overview

This project demonstrates an **end-to-end data engineering solution** built using **Microsoft Fabric**, implementing the **Medallion Architecture (Bronze, Silver, Gold)**.

The solution simulates a retail use case (**Shopping Mart**) to process and analyze data related to **orders, customers, products and reviews**, enabling business insights through a Power BI dashboard.

---

## 🏗️ Architecture Overview

The architecture follows a layered approach:

**Git Source → Bronze (Raw) → Silver (Transformed) → Gold (Business Layer) → Semantic Model → Power BI Reports**

<img width="1027" height="490" alt="image" src="https://github.com/user-attachments/assets/ab9c7cb0-c686-4e26-a8f1-b9beade01ab1" />


* Data is ingested from a Git repository using **metadata-driven pipelines**
* Processed using **PySpark notebooks**
* Utilizing **Shortcuts** and **Materialized Lake Views (MLVs)**
* Consumed via **Power BI Semantic Model and Reports**

---

## ⚙️ Key Features

* ✅ Metadata-driven ingestion using JSON configuration
* ✅ Multi-Lakehouse architecture (Bronze, Silver, Gold separation)
* ✅ PySpark-based transformations
* ✅ Shortcuts and Materialized Lake Views (MLVs) for performance optimization
* ✅ End-to-end pipeline orchestration in Microsoft Fabric
* ✅ Semantic modeling for reporting
* ✅ Power BI dashboards for visualization

---

## 🧱 Bronze Layer (Raw Data)

* Data ingested from Git repository
* Controlled using metadata configuration
* Stored in raw format without transformations
  ## *Data Pipeline*
<img width="932" height="424" alt="image" src="https://github.com/user-attachments/assets/c0ea19a0-ded1-4058-ad51-f69868be1563" />

  ## *Bronze Lakehouse*
<img width="953" height="303" alt="image" src="https://github.com/user-attachments/assets/24620940-5aa9-4cdf-b569-b29fbd3fe49c" />

👉 Refer to `bronze/` folder for details

---

## 🔧 Silver Layer (Transformation)

* Data cleansing and transformation using PySpark
  ## *Silver Notebook*
<img width="608" height="407" alt="image" src="https://github.com/user-attachments/assets/3b474bcb-5aa3-4d76-b2c9-2e74b651ac87" />

  ## *Silver Lakehouse*
<img width="667" height="407" alt="image" src="https://github.com/user-attachments/assets/ecfe47f5-79ae-4849-a312-36dab6bf7bc5" />

👉 Refer to `silver/` folder for notebook

---

## 📊 Gold Layer (Business Layer)

* Creating Shortcuts and **Materialized Lake Views (MLVs)**
* Aggregated datasets for business reporting

## *Gold Notebook*
<img width="461" height="412" alt="image" src="https://github.com/user-attachments/assets/92388c2d-1d4d-4022-b539-f24ba2e90f16" />

## *Gold Lakehouse*
<img width="629" height="383" alt="image" src="https://github.com/user-attachments/assets/ec0073bf-2a27-439f-9553-f21762b3b970" />

👉 Refer to `gold/` folder

---
## 🔄 Final Pipeline Orchestration

<img width="770" height="392" alt="image" src="https://github.com/user-attachments/assets/022d0e6d-d0dd-42c9-9ad5-2324aef00317" />


## 📈 Power BI Report

The final layer provides business insights through interactive reports.
<img width="790" height="427" alt="image" src="https://github.com/user-attachments/assets/b6eb9fc8-a886-4c4a-bf39-3197f0e9fd15" />


---

## 🔥 Conclusion

This project showcases a **production-style modern data platform** using Microsoft Fabric, combining data engineering, transformation, and analytics into a unified solution.
  ## *Lineage View*
<img width="536" height="385" alt="image" src="https://github.com/user-attachments/assets/6a4a7413-95ce-4967-9081-f36bf3e33f37" />
