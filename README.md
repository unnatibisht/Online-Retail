# Global Wholesale & Retail Transaction Analysis: Online Retail II

An end-to-end data analytics project focused on cleaning, processing, and analyzing over 1 million international commercial transactions from the Online Retail II dataset. This project establishes a rigorous data foundation designed to handle messy real-world transaction logs and extract clean business intelligence metrics.

## 📌 Project Overview
The goal of this project is to transform chaotic, raw transactional data into a reliable foundation for business analysis. By building a strict data cleaning pipeline, the project isolates true sales performance, eliminates data leakage from cancellations or test entries, and accurately surfaces the top revenue-generating products.

---

## 🛠️ The Data Engineering Challenge
Real-world transactional datasets often suffer from formatting anomalies, missing values, and mixed-type constraints. Key data challenges resolved in this pipeline include:
* **Invalid Cancellations & Noise:** Filtering out rows containing negative quantities, zero-prices, and invoice numbers prefixed with 'C' (cancellations).
* **DataType Corruption (`IntCastingNaNError`):** Handling missing customer records that trigger standard integer conversion crashes during pipeline execution.
* **String Decimal Formatting:** Stripping unwanted trailing decimals from identifier fields cleanly without preserving hidden text-based null artifacts.
* **Separating Logistics from Retail:** Isolating internal service fees (such as postage and manual processing fees) from actual retail inventory to ensure true product performance reporting.

---

## 📊 Data Visualizations & Strategic Rationales

### 1. Monthly Revenue by Time
<img src="./Pictures/Screenshots/Monthly%20Revenue%20by%20Time.png" alt="Monthly Revenue by Time" width="100%">

* **Why I Chose This:** 
  Tracking the monthly trajectory allows stakeholders to see the macroeconomic pulse of the business. By looking at this exact timeline chart, we can clearly identify cyclical shopping behavior, major seasonal surges towards the final quarters of the year, and baseline operational dips. This insight is crucial for planning inventory stock levels and optimizing marketing budget allocation before peak demand hits.

---

### 2. Top 10 Products by Revenue
<img src="./Pictures/Screenshots/Top%2010%20Products%20by%20Revenue.png" alt="Top 10 Products by Revenue" width="100%">

* **Why I Chose This:** 
  I chose a horizontal ranking chart to explicitly expose top revenue-drivers like the `REGENCY CAKESTAND 3 TIER` alongside service constraints like `DOTCOM POSTAGE` and `POSTAGE`. Visualizing this is a critical diagnostic step in retail data engineering: it proves why we need to separate logistics fees from actual product inventory. This ensures that stock optimization, warehouse space allocation, and purchasing strategy are driven purely by commercial inventory assets rather than shipping overhead.

---

## 📈 Business Insights & Impact
* **Data Volume Optimization:** Streamlined the dataset down to valid, revenue-generating customer profiles.
* **Pure Product Analytics:** By surfacing overhead metrics like postage fees in our preliminary graphs, we can successfully decouple service costs from physical inventory logic.
* **Downstream Readiness:** The finalized dataset features perfectly formatted, standardized customer metrics, making it instantly compatible with advanced analytics like RFM segmentation, monthly trend analysis, and cohort retention models.

## 💻 Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Environment:** Jupyter Notebook

## 🏁 Conclusion
Data science isn't just about building flashy models; it's about building a robust data foundation. By systematically addressing type constraints, unmasking hidden null values, and separating operational overhead from true retail data, this project transforms raw, chaotic transaction logs into highly accurate, deployment-ready business intelligence.
