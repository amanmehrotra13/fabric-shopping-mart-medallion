# Metadata Configuration for Ingestion

## 📌 Overview

The Bronze layer raw data ingestion is implemented using a **metadata-driven approach**, where ingestion logic is dynamically controlled using metadata files.

This eliminates hardcoding and enables scalable ingestion of multiple datasets.

---

## 🔑 Field Definitions

| Field Name    | Description                            |
| ------------- | -------------------------------------- |
| `source_url`  | Path of the file in the Git repository |
| `sink_folder` | Target folder in Bronze Lakehouse      |
| `sink_file`   | Output file name stored in Lakehouse   |

---

## ⚙️ How It Works

1. The pipeline reads the metadata configuration
2. Iterates over each entry
3. Dynamically ingests data from Git source
4. Writes data into the Bronze Lakehouse

This allows ingestion of multiple datasets using a single reusable pipeline. Please refer screenshots of data pipelines and lakehouse from readme.

---

## 🚀 Benefits

* Eliminates hardcoded ingestion logic
* Easily scalable for new datasets
* Centralized configuration
* Improves maintainability
* Enables dynamic pipeline execution

---

## 📌 Summary

This metadata-driven approach provides a flexible and scalable ingestion framework, forming a strong foundation for the Bronze layer in the Medallion Architecture.
