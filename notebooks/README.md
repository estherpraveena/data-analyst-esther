# 📊 Vancouver Rental Standards Data Pipeline (AWS + Python Project)

This project is a complete **data analytics and engineering portfolio** built using a real-world dataset from the [City of Vancouver’s Rental Standards](https://opendata.vancouver.ca/explore/dataset/rental-standards-current-issues). It showcases the entire data lifecycle: from ingestion and wrangling to profiling, enrichment, governance, and visualization using **AWS tools** and **Python**.

---

## 🎯 Project Objective

To build a cloud-based data pipeline that collects, cleans, analyzes, and monitors rental bylaw violation data, using:

- **AWS Glue & DataBrew** for transformation
- **S3** for storage
- **KMS & IAM** for security
- **CloudWatch** for observability
- **Python** (Pandas, Matplotlib) for notebook-based analysis

---

## 📁 Project Structure

📦 data-analyst-esther/ ├── data/ # Raw dataset (.csv) ├── notebooks/ # Jupyter notebooks for profiling & cleaning ├── portfolio/ # Winter-style writeups (EDA, Wrangling, Quality) ├── aws/ # AWS-based documentation (DataBrew, Governance) ├── README.md # This file

---

## 🧰 Tools and Technologies

| Category | Tools |
|---------|-------|
| 🧪 Analysis | Python, Pandas, Matplotlib, Seaborn |
| ☁️ Cloud | AWS S3, AWS Glue, AWS DataBrew |
| 🔐 Security | AWS KMS, IAM |
| 📈 Monitoring | AWS CloudWatch |
| 🧹 Wrangling | DataBrew recipes, Jupyter notebooks |
| 📊 Visualization | Jupyter Notebook (Bar charts, group-by summaries) |

---

## 📌 Key Steps

- **Data Wrangling:** Cleaned and standardized rental violation data using AWS Glue and Python
- **Data Profiling:** Analyzed completeness, missing values, and outliers using Pandas and DataBrew
- **Data Quality Control:** Enforced governance rules (pass/fail folders) and real-time alerting via CloudWatch
- **Visualization:** Created notebooks to summarize patterns by business, location, and more

---

## 📄 Portfolio Writeups

Each stage of the project is written as a Winter Portfolio module:

- 📂 [`portfolio/data_wrangling.md`](./portfolio/data_wrangling.md)
- 📂 [`portfolio/descriptive_analysis.md`](./portfolio/descriptive_analysis.md)
- 📂 [`portfolio/exploratory_analysis.md`](./portfolio/exploratory_analysis.md)
- 📂 [`portfolio/data_quality_control.md`](./portfolio/data_quality_control.md)

---

## 🔒 AWS Workflow & Governance

AWS implementation is documented separately:

- 🔧 [`aws/databrew_workflow.md`](./aws/databrew_workflow.md)
- 🛡️ [`aws/governance_observability.md`](./aws/governance_observability.md)

---

## 📌 Dataset

- **Source:** [City of Vancouver Open Data](https://opendata.vancouver.ca/explore/dataset/rental-standards-current-issues)
- **Details:** Contains rental property bylaw infractions, geographic info, and inspection status.

---

## 🚀 Author

**Esther Praveena**  
Aspiring Data Analyst | AWS Learner | Open to opportunities  
[LinkedIn](#) • [GitHub](#) • [Portfolio](#)

---

