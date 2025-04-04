
# 📊 Railway Analysis Demo Use Case (Azure Data Engineering)

## 👨‍💻 Author
**Yash Shah** – Data Engineering Specialist

---

## 📁 Project Overview

This end-to-end demo use case showcases the power of modern **Azure Data Engineering** services, specifically **Azure Data Factory** and **Azure Databricks**, to analyze Indian Railway operational data. It simulates a real-world scenario where data is extracted from multiple sources, transformed, and stored for further business intelligence and analytics.

---

## 🏗️ Architecture Components

- **Source**: CSV and JSON files (simulating public datasets)
- **Ingestion**: Azure Data Factory
- **Storage**: Azure Data Lake Storage Gen2
- **Processing**: Azure Databricks using PySpark
- **Output Layer**: Delta Lake (Gold Layer)
- **Orchestration**: ADF Pipelines using Parameterized JSON templates

---

## 📂 Project Structure

```
.
├── Parameter_File_For_ADF/
│   └── Parameters.json
├── Source_Dataset/
│   ├── railway_details.csv
│   ├── delay_details.json
│   └── satisfaction_details.json
├── Use_Case_ADF_Files/
│   ├── dataset/
│   ├── linkedService/
│   ├── pipeline/
│   └── info.txt
├── Use_Case_Databricks_Code_Export/
│   ├── main.py
│   ├── delay_details_silver_deltaload.py
│   └── gold_analysis_load.py
```

---

## 🔗 Data Sources & Structure

| File | Type | Description |
|------|------|-------------|
| `railway_details.csv` | Structured | Railway operations, PNR, Train metadata |
| `delay_details.json` | Semi-structured | Delay reason mappings |
| `satisfaction_details.json` | Semi-structured | Customer survey feedback |

---

## 🔄 Pipeline Flow

1. **Ingestion Layer (Bronze)**: ADF pipelines load raw data into ADLS.
2. **Transformation Layer (Silver)**: Databricks notebooks clean and merge datasets using Delta format.
3. **Analysis Layer (Gold)**: Aggregated and analytical insights created for final reporting.

---

## ⚙️ Frequency & Volume

- **Data Frequency**: Daily batch loads (simulated)
- **Volume**: Small demo scale, can be scaled to GBs or TBs in enterprise use
- **File Format to Downstream**: Delta Table (Parquet), optionally CSV/JSON for external tools

---

## 🧪 Notebooks Summary

- `main.py` – Entry point that triggers the flow
- `delay_details_silver_deltaload.py` – Cleans delay JSON data into Silver layer
- `gold_analysis_load.py` – Aggregates Silver data for BI reporting

---

## ✅ Key Features

- Modular parameterized ADF pipelines
- Delta Lake implementation for versioned and performant queries
- Clean code with PySpark best practices
- Scalable and production-like structure for hands-on demonstration

---

## 🧠 What You’ll Learn

- Real-time cloud data engineering workflow on Azure
- Building end-to-end pipelines with ADF + Databricks
- Handling semi-structured & structured datasets
- Data modeling: Bronze → Silver → Gold

---

## 📌 Future Scope

- Integrate Power BI or Synapse for visualization
- Add schema enforcement and unit testing in Databricks
- Implement CI/CD via Azure DevOps pipelines
