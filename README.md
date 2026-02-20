# AWS Data Lake Project – Parquet Partitioning with Athena

## 📌 Project Overview

This project demonstrates a data persistence workflow using columnar storage (Parquet) and partitioning strategies in AWS.

The dataset was processed using Pandas and persisted in both CSV and Parquet formats. The Parquet files were compressed using Snappy and partitioned by `reference_date`.

The data was uploaded to Amazon S3 and queried using Amazon Athena through an external table.

---

## 🛠 Technologies Used

- Python
- Pandas
- PyArrow
- Amazon S3
- Amazon Athena
- SQL

---

## ⚙️ Workflow

1. Data ingestion with Pandas  
2. Column normalization  
3. Creation of partition column (`reference_date`)  
4. Data persistence in CSV and Parquet  
5. Upload to S3  
6. External table creation in Athena  
7. Partition repair (`MSCK REPAIR TABLE`)  
8. Query validation  

---

## 🚀 Key Concepts

- Columnar storage (Parquet)
- Data partitioning
- Serverless SQL querying
- Data lake fundamentals
- Query performance optimization

---

## 📊 Architecture

Data → Pandas → Parquet (Partitioned) → S3 → Athena → SQL
