# 🧹 Portfolio Project: Data Wrangling

## 🎯 Objective

The objective of this module was to demonstrate effective **data wrangling** using both **AWS DataBrew** and **Python notebooks**. The dataset used contains rental standards and bylaw violation information from the City of Vancouver.

---

## 🔗 Dataset

- Source: [City of Vancouver Open Data Portal](https://opendata.vancouver.ca/explore/dataset/rental-standards-current-issues)
- Format: CSV
- Size: ~2,000 rows
- Raw Issues: Missing values, unstructured columns, semicolon delimiters, combined location data

---

## 🔧 Tools Used

| Type       | Tools |
|------------|-------|
| Cloud      | AWS S3, AWS Glue DataBrew |
| Scripting  | Google Colab (Python, Pandas) |
| Notebook   | `data_cleaning.ipynb` |
| Language   | Python |
| File Format| CSV with `;` separator |

---

## 🛠️ Wrangling Steps (Python - `data_cleaning.ipynb`)

The following steps were performed in a Colab notebook:

1. **Read CSV with custom delimiter**
   - Used `pd.read_csv(url, delimiter=';')` to properly parse the dataset.
2. **Column Cleanup**
   - Stripped leading/trailing spaces using `df.columns.str.strip()`.
3. **Missing Values**
   - Dropped rows with missing geolocation using `dropna(subset=['geo_point_2d'])`.
4. **Split Coordinates**
   - Separated the `geo_point_2d` column into `Latitude` and `Longitude`.
5. **Dropped Unnecessary Columns**
   - Removed redundant or merged columns like `geo_point_2d` after extraction.

---

## 🔁 Wrangling in AWS Glue DataBrew

The same dataset was also wrangled using **AWS DataBrew** to demonstrate no-code data processing:

| Task | Performed In |
|------|--------------|
| Remove null rows | DataBrew recipe |
| Rename columns | DataBrew recipe |
| Standardize column case | DataBrew recipe |
| Format columns (string trimming) | DataBrew recipe |
| Profile job (to check missing values, types) | AWS Glue DataBrew |

---

## ✅ Output

- Cleaned dataset with separate Latitude and Longitude columns
- No missing critical values
- Final version saved and used for further analysis in `data_summary.ipynb`

---

## 📂 Files Related to This Module

- [`data_cleaning.ipynb`](../notebooks/data_cleaning.ipynb)
- [`rental-standards-current-issues.csv`](../data/rental-standards-current-issues.csv)
- AWS Work: Documented in [`aws/databrew_workflow.md`](../aws/databrew_workflow.md)

---
