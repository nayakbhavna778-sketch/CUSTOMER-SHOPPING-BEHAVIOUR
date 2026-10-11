# 🛍️ Online Shopping Customer Behaviour Analysis

An end-to-end data analytics project that explores **how customers shop online and what influences their spending**. The project covers data cleaning and EDA in **Python**, business analysis in **SQL**, and an interactive dashboard in **Power BI**.

---

## 📊 Dashboard Preview

![Customer Shopping Behaviour Dashboard](dashboard%20preview.jpeg)

---

## 📌 Project Overview

Understanding customer behaviour helps an online store decide which products to promote, which markets and devices to focus on, and which customers to target. This project analyses **1,800 customer records** to see how spending varies by product category, country, gender, device and age group, and whether browsing behaviour is linked to spending.

**Key numbers**

| Metric | Value |
|--------|-------|
| Total customers | 1,800 |
| Columns | 10 |
| Missing values | None |
| Duplicate records | None |
| Total spending | $1,401,306 |
| Average spend per customer | ~$778 (range $5 to $1,499) |
| Average time spent on the platform | ~60.5 minutes |

---

## 🎯 Objectives

- Inspect the dataset and check its quality (data types, missing values, duplicates)
- Explore the data visually to understand customer and product patterns
- Compare spending across product categories, countries, genders, devices and age groups
- Check whether age, time spent and items viewed are related to spending
- Identify high-value customers and customers who browse a lot but buy little
- Present the findings in an interactive Power BI dashboard

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| **Python (pandas, Matplotlib, Seaborn, Plotly)** | Data inspection, cleaning and EDA |
| **SQL (MySQL)** | Business analysis queries |
| **Power BI** | Interactive dashboard and visualisation |
| **Jupyter / Google Colab** | Notebook environment |

---

## 🗂️ Dataset Description

| Column | Description |
|--------|-------------|
| `customer_id` | Unique ID of each customer (`CUST_1` to `CUST_1800`) |
| `gender` | Gender of the customer (Male / Female) |
| `age` | Age of the customer in years |
| `country` | Country of the customer (6 countries) |
| `device_type` | Device used for shopping (Mobile / Desktop / Tablet) |
| `product_category` | Product category (6 categories) |
| `time_spent_minutes` | Time spent on the platform, in minutes |
| `items_viewed` | Number of items viewed |
| `items_purchased` | Number of items purchased |
| `total_spent_usd` | Total amount spent, in US dollars |

---

## 📂 Repository Contents

| File | Description |
|------|-------------|
| `CUSTOMER SHOPPING BEHAVIOUR CLEANING.ipynb` | Python notebook with data inspection, cleaning checks and EDA |
| `CLEANED CUSTOMER SHOPPING BEHAVIOUR.csv` | Cleaned dataset used for SQL and Power BI |
| `SQL QUERIES.sql` | SQL queries for category, country, gender, device, age group and customer analysis |
| `CUSTOMER SHOPPING BEHAVIOUR.pbix` | Interactive Power BI dashboard |
| `dashboard preview.jpeg` | Screenshot of the dashboard |
| `README.md` | Project documentation |

---

## 🔄 Project Workflow

### 1. Data Cleaning & EDA (Python)
- Loaded the dataset and checked its structure with `shape`, `info()`, `head()` and `tail()`
- Checked for **missing values** and **duplicate records** (none found)
- Reviewed summary statistics for numeric and text columns
- Explored product categories with Matplotlib, Seaborn and Plotly charts
- Built 3D scatter plots of age, time spent and total spent
- Plotted a **correlation heatmap** of the numeric columns

### 2. Data Analysis (SQL)
Queries written to answer questions such as:
- How many customer records are there?
- Which product categories have the highest average spending?
- Which countries bring in the most total spending?
- How do male and female customers compare in items purchased and spending?
- Which device type has the highest average spending?
- Which customers spend more than the average customer?
- Which age group spends the most?
- Does more time spent on the platform mean more spending, by category?
- Which customers view many items but buy very little?
- How can customers be segmented into High, Medium and Low spenders?
- Who are the top 3 spenders in each country?

### 3. Dashboard (Power BI)
An interactive one-page dashboard titled **"Customer Shopping Behaviour"**.
- **Filters:** gender, age group, country, device type and product category
- **KPI cards:** Total Customers (1.8K), Total Purchased (8K items), Total Spending ($1,401,306) and Average Time Spent (60.54 minutes)
- **Charts:** top 5 product categories by average spending, spending by country, gender-wise purchase behaviour, device-wise spending share, average spending by age group, and top 10 customers by spending

---

## 💡 Business Insights

**From the Python EDA**
- **Clean data:** 1,800 customers, no missing values or duplicates.
- **Popular categories:** Clothing leads with **345** customers, followed by Sports (311), Electronics and Books (294 each), Beauty (283) and Home (273). Customers are spread fairly evenly across categories.
- **Customer mix:** Male and female customers are almost evenly split (911 male). Pakistan is the most common country (330 customers) and Tablet is the most used device (637 customers).
- **Spending:** The average customer spends about **$778**, with a median of **$802**.
- **Weak correlations:** Total spending shows almost **no correlation** with age, time spent, items viewed or items purchased (all between 0.01 and 0.03). Spending more time on the platform or viewing more items does not by itself mean a customer spends more.

**From the Power BI dashboard**
- **Overall:** 1.8K customers generated a total spending of **$1,401,306** and purchased about 8K items, with customers spending around **60.5 minutes** on the platform on average.
- **Category spending:** **Clothing** has the highest average spending, followed by Electronics, Beauty, Sports and Home. **Books** falls outside the top 5. The bars are close in height, so the gap between categories is small.
- **Countries:** **Pakistan** has the highest total spending, followed by USA, Canada, Australia, UK and India. Pakistan also has the most customers (330), so part of its lead comes from having a bigger customer base.
- **Gender:** Male and female customers purchase almost the same number of items on average, with male customers slightly ahead.
- **Devices:** Spending is split almost evenly across devices: **Tablet 36.13%**, **Desktop 32.75%** and **Mobile 31.12%**.
- **Age groups:** Average spending is lowest for customers **below 25**, rises to a peak around the **35-44** group and dips slightly for **45 and above**. The difference between age groups is small (roughly $740 to $785).
- **Top customers:** The top 10 customers (for example CUST_1326, CUST_922 and CUST_537) all spent close to the maximum of about $1,500.
- **Spending segments (SQL):** `[ADD: share of High / Medium / Low spenders]`

---

## ✅ Business Recommendations

> Based on the insights above, the business can consider the following actions. Keep the points that your results support and remove the rest.

1. **Do not rely on time spent or items viewed alone.** Since they show almost no link with spending, use other signals such as product category, device and country to decide where to focus.
2. **Promote strong categories and support weaker ones.** Clothing is the most popular category and also has the highest average spending, so keep stock and marketing strong there. Run offers on Home (fewest customers) and Books (outside the top 5 for average spending).
3. **Target "window shoppers".** Customers who view many items but buy very little can be reached with reminders, discounts or an easier checkout.
4. **Reward high spenders.** Use the High / Medium / Low segmentation to offer loyalty benefits to top customers and upgrade offers to the medium group.
5. **Focus on the best markets and devices.** Pakistan and USA bring in the most spending, so keep investing there and look for ways to grow weaker markets like India. Since spending is split almost evenly across Tablet, Desktop and Mobile, keep the shopping experience equally smooth on all three.
6. **Track results regularly.** Use the Power BI dashboard to monitor spending by category, country and device over time.

---

## 🏁 Conclusion

This project analysed **1,800 online shopping customers** across 10 columns. The data was clean, with no missing values or duplicates. Customers were spread fairly evenly across six product categories, with Clothing the most popular, and the average customer spent about $778.

The most notable finding is that **age, time spent, items viewed and items purchased have almost no correlation with total spending**, so simple behaviour numbers do not explain how much a customer spends. The dashboard shows that Clothing has the highest average spending and Pakistan the highest total spending, while differences across devices, genders and age groups are small.

Using **Python** for EDA, **SQL** for business analysis and **Power BI** for visualisation, the project gives a clear view of customer behaviour that can guide marketing, product and customer-targeting decisions.

**Future scope:** build a customer segmentation or spending-prediction model using additional features such as purchase history.

---

## 🚀 How to Use This Project

1. Clone the repository
   ```bash
   git clone https://github.com/nayakbhavna778-sketch/CUSTOMER-SHOPPING-BEHAVIOUR.git
   ```
2. Open `CUSTOMER SHOPPING BEHAVIOUR CLEANING.ipynb` in Jupyter Notebook or Google Colab to view the cleaning and EDA steps.
3. Run `SQL QUERIES.sql` in MySQL after loading `CLEANED CUSTOMER SHOPPING BEHAVIOUR.csv` into the `shopping` table. The `customer_id` values are text (`CUST_1`, `CUST_2`, ...), so that column should be created as `VARCHAR`, not `INT`.
4. Open `CUSTOMER SHOPPING BEHAVIOUR.pbix` in Power BI Desktop to explore the dashboard.

---

## 👩‍💻 About Me

Hi, I'm **Riddhi**, a student based in Delhi, India, with a growing interest in data analytics. I enjoy turning raw data into clear insights and I work with **Python (pandas, NumPy), SQL, Power BI and Tableau**.

This project is part of my data analytics portfolio, where I practise the full workflow: cleaning data, analysing it with SQL and presenting it visually.

📫 **Connect with me:** [LinkedIn](add-your-link) | [Email](mailto:add-your-email)

---

⭐ If you found this project useful, feel free to star the repository!
