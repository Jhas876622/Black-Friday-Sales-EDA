# Black Friday Sales Data Analysis

> **Repository:** `black-friday-sales-analysis`
> **Author:** [@jhas876622](https://github.com/jhas876622)

---

## 📌 Project Overview

This project is an **end‑to‑end exploratory data analysis (EDA)** and **business insight** project based on **Black Friday Sales** data.

The main goals are:

* 🛒 Understand **customer purchasing behavior** during Black Friday.
* 👥 Analyze how **age, gender, city, and occupation** affect spending.
* 🧺 Identify **high‑value customer segments** and product categories.
* 💼 Present insights that a **business / management team** can use for:

  * Targeted marketing
  * Better discount strategies
  * Inventory planning

This project is designed to showcase **strong data analytics, business thinking, and clear storytelling**, suitable for adding to a **Data Analyst / Business Analyst resume or portfolio**.

---

## 🗂️ Dataset

* **Name:** Black Friday Sales Dataset
* **Source:** Public retail transaction dataset (commonly available on platforms like Kaggle)
* **Rows:** ~500,000+ transactions (depending on version)
* **Type:** Structured, tabular data

### 📄 Key Columns (Typical)

| Column Name                  | Description                                    |
| ---------------------------- | ---------------------------------------------- |
| `User_ID`                    | Unique ID of the customer                      |
| `Gender`                     | Gender of the customer (M/F)                   |
| `Age`                        | Age group (e.g., 0-17, 18-25, 26-35, etc.)     |
| `Occupation`                 | Encoded occupation category                    |
| `City_Category`              | Category of the city (A, B, C)                 |
| `Stay_In_Current_City_Years` | No. of years living in current city            |
| `Marital_Status`             | 0 = Unmarried, 1 = Married                     |
| `Product_ID`                 | Unique ID of the product                       |
| `Product_Category_1/2/3`     | Encoded product category features              |
| `Purchase`                   | Purchase amount (target variable for analysis) |

> ⚠️ **Note:** If your dataset schema is slightly different, you can adjust this section accordingly.

---

## 🎯 Business & Analytics Objectives

1. **Who are the top spending customer segments?**
2. **Which age and gender groups spend the most?**
3. **Which city category contributes maximum revenue?**
4. **What product categories perform best?**
5. **What insights can support better marketing and discount decisions?**

---

## 🧪 Tech Stack & Tools

* **Language:** Python
* **Environment:** Jupyter Notebook (`Black Friday Sales Data Analyis.ipynb`)
* **Libraries (typical):**

  * `pandas` – data manipulation
  * `numpy` – numerical operations
  * `matplotlib` / `seaborn` – data visualization
  * `plotly` / `cufflinks` (optional) – interactive plots

```bash
# Example: install dependencies
pip install pandas numpy matplotlib seaborn plotly jupyter
```

---

## 📁 Project Structure

```bash
black-friday-sales-analysis/
├── data/
│   └── BlackFriday.csv          # Raw dataset (not committed if large)
├── notebooks/
│   └── Black Friday Sales Data Analyis.ipynb
├── images/
│   └── plots_*.png              # Exported plots/visuals (optional)
├── README.md
└── requirements.txt             # Python dependencies (optional)
```

> 💡 You can adjust folder names as per your actual project.

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/jhas876622/black-friday-sales-analysis.git
cd black-friday-sales-analysis
```

### 2️⃣ (Optional) Create & Activate Virtual Environment

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS / Linux
python3 -m venv venv
source venv/bin/activate
```

### 3️⃣ Install Requirements

If you have a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Or manually install core libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

### 4️⃣ Run the Notebook

```bash
jupyter notebook
```

Then open:

* `notebooks/Black Friday Sales Data Analyis.ipynb`

---

## 🧠 Analysis Workflow

A typical flow followed in the notebook:

1. **Import Libraries & Load Data**

   * Load CSV file into pandas DataFrame.

2. **Understand the Data**

   * Check shape, types, missing values, basic statistics.

3. **Data Cleaning & Pre‑Processing**

   * Handle missing values (e.g., product categories).
   * Convert columns to appropriate types (categorical, numeric).
   * Optional: Create new features (e.g., total products per user, spending range, etc.).

4. **Univariate Analysis**

   * Distribution of `Purchase`.
   * Count plots for `Gender`, `Age`, `City_Category`, etc.

5. **Bivariate / Multivariate Analysis**

   * Average `Purchase` by `Gender`, `Age`, `City_Category`.
   * Grouped bar charts and boxplots.
   * Heatmaps / correlation plots (where relevant).

6. **Customer Segmentation View (Analytics / Business Angle)**

   * Identify high‑spending age+gender combinations.
   * Top performing city categories.
   * High‑value product categories.

7. **Insights & Business Recommendations**

   * Translate charts into clear business actions.

---

## 📊 Key Insights (Example Style)

You can adapt this section based on your actual results from the notebook:

* **Age Group 26–35** shows the **highest total and average purchase amount**, making it a key target segment.
* **Male customers** may have higher total spending (due to higher count), but **females** might show higher **average** purchase in certain categories.
* **City Category B** (for example) could contribute a large share of revenue, indicating strong demand and growth potential.
* Certain **product categories** repeatedly appear in top revenue lists, suggesting they are ideal for **bundling and promotions**.

> ✍️ Replace these bullets with your exact insights once your analysis is finalized.

---

## 🧾 Sample Code Snippet

```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Load data
df = pd.read_csv("data/BlackFriday.csv")

# Basic info
print(df.head())
print(df.info())

# Average purchase by age group
age_purchase = df.groupby("Age")["Purchase"].mean().sort_values(ascending=False)
print(age_purchase)

sns.barplot(x=age_purchase.index, y=age_purchase.values)
plt.title("Average Purchase by Age Group")
plt.xlabel("Age Group")
plt.ylabel("Average Purchase Amount")
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

---

## 🧩 Example Use Cases (Business Angle)

* **Marketing Team** → Identify which age + gender + city segments to target for Black Friday campaigns.
* **Product Team** → Focus on high‑performing product categories and bundles.
* **Finance / Management** → Understand revenue drivers and discount impact.
* **Data Portfolio** → Showcase SQL + Python + EDA + visualization + insight storytelling.

---

## ✅ To‑Do / Future Work

* [ ] Add **SQL queries** for pre‑processing / aggregations (if using a database).
* [ ] Create a **dashboard** (Power BI / Tableau / Streamlit) using the final cleaned dataset.
* [ ] Add **machine learning model** for predicting purchase amount (optional).
* [ ] Improve visualizations with interactive charts.

---

## 🤝 Contributing

Contributions, ideas, and suggestions are welcome!

1. Fork the repo
2. Create a new branch (`feature/new-analysis`)
3. Commit your changes
4. Open a Pull Request

---

## 📬 Contact

If you like this project or want to collaborate:

* **GitHub:** [@jhas876622](https://github.com/jhas876622)
* **Email:** jha876622@gmail.com

## thankyou---
