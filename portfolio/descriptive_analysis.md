# 📊 Portfolio Project: Descriptive Analysis
 
 ## 🎯 Objective
 
 The goal of this module was to perform **descriptive analysis** on the raw rental standards dataset. This step helps identify the basic structure, data types, missing values, and high-level distributions within the data before proceeding to deeper analytics.
 
 ---
 
 ## 🔗 Dataset Summary
 
 - 📁 File: `rental-standards-current-issues.csv`
 - 🔣 Source: [City of Vancouver Open Data](https://opendata.vancouver.ca/explore/dataset/rental-standards-current-issues)
 - 📏 Shape: ~2,000 rows × 9 columns
 - 📌 Key columns:
   - `BUSINESSOPERATOR`
   - `Geo Local Area`
   - `TOTALOUTSTANDING`
   - `geo_point_2d`
 
 ---
 
 ## 🧰 Tools Used
 
 | Type       | Tools |
 |------------|-------|
 | Scripting  | Google Colab |
 | Libraries  | Python (Pandas, Matplotlib, Seaborn) |
 | Cloud (optional) | AWS Glue DataBrew (Profiling Job) |
 
 ---
 
 ## 🔍 Descriptive Profiling (Notebook)
 
 Performed in `data_profiling.ipynb`:
 
 1. **Column Types**
    - Identified strings, floats, and nulls using `df.info()`
 
 2. **Missing Values**
    - Counted using `df.isnull().sum()`
    - Found missing values mainly in `geo_point_2d` and address fields
 
 3. **Statistical Summary**
    - Used `df.describe()` to get mean, std, min, max of numerical columns
    - Key stats observed for `TOTALOUTSTANDING` and `TotalUnits`
 
 4. **Value Counts**
    - Top 10 `BUSINESSOPERATOR` entries
    - Top 10 `Geo Local Area` entries
 
 ---
 
 ## 🧪 Sample Code Snippets
 
 ```python
 # Check missing values
 df.isnull().sum()
 
 # Summary stats
 df.describe()
 
 # Top areas
 df['Geo Local Area'].value_counts().head(10)
 
 # Top operators
 df['BUSINESSOPERATOR'].value_counts().head(10)
