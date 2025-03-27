# 🔍 Portfolio Project: Exploratory Analysis

## 🎯 Objective

The purpose of this stage was to conduct **exploratory data analysis (EDA)** to uncover patterns, correlations, and visual insights that could inform decision-making.

---

## 🧰 Tools Used

| Type         | Tools              |
|--------------|--------------------|
| Notebook     | `data_summary.ipynb` |
| Platform     | Google Colab       |
| Libraries    | Pandas, Matplotlib, Seaborn |

---

## 📊 Key Visualizations & Findings

All visuals were created in [`data_summary.ipynb`](../notebooks/data_summary.ipynb).

---

### 1. 🏙️ Top 10 Geo Areas by Violation Count

> **Insight:** Neighborhoods like Downtown and Renfrew-Collingwood showed significantly higher violation volumes. These areas may have higher population density or aging rental infrastructure.

- Used `.value_counts()` on `Geo Local Area`
- Visualized using `seaborn.barplot()` with horizontal bars

---

### 2. 🧑‍💼 Top 10 Business Operators with Most Violations

> **Insight:** A small set of operators contributed to a large number of violations. These could be prioritized for inspection or outreach.

- Counted using `.value_counts()` on `BUSINESSOPERATOR`
- Visualized using bar chart

---

### 3. 💰 Average Total Outstanding by Area

> **Insight:** Certain areas (like West End and Downtown) not only had more violations but also higher average unpaid balances, possibly reflecting larger buildings or stricter enforcement.

- Grouped using `.groupby('Geo Local Area')`
- Used `.mean()` on `TOTALOUTSTANDING`
- Sorted and plotted top 10

---

## 📸 Sample Code Snippet

```python
# Visualize top 10 Geo Areas
top_areas = df['Geo Local Area'].value_counts().head(10)

plt.figure(figsize=(10,6))
sns.barplot(x=top_areas.values, y=top_areas.index)
plt.title('Top 10 Areas by Violation Count')
plt.xlabel('Violations')
plt.ylabel('Geo Local Area')
plt.tight_layout()
plt.show()
```

---

## 💡 Interpretation

- 🔥 **Hotspot Areas**: Downtown and Mount Pleasant may need focused city resources.
- 🧾 **Frequent Offenders**: A handful of operators are responsible for repeat violations.
- 💸 **Outstanding Fines**: Financial metrics could help prioritize enforcement or support.

---

## 📂 Files Linked

- [`data_summary.ipynb`](../notebooks/data_summary.ipynb)
- [`rental-standards-current-issues.csv`](../data/rental-standards-current-issues.csv)

---
