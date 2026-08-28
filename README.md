# Customer Segmentation & RFM Analysis

Customer segmentation project using **RFM analysis** and **K-Means clustering** to identify high-value customers, customers with potential inactivity, and opportunities for revenue recovery.

The analysis translates customer purchasing behavior into actionable business strategies for **retention, reactivation, and customer development**.

---

## 1. Business Problem

The company has a large customer base but lacks a clear understanding of customer value and purchasing behavior. Without effective segmentation, marketing resources may be allocated uniformly, making it difficult to prioritize high-value customers and identify potential reactivation opportunities.

### Main Question

> **How can we segment customers based on their purchasing behavior to identify high-value and potentially inactive customers, and what strategies can be implemented to improve retention and revenue?**

### Business Objectives

* Identify high-value and highly engaged customers.
* Identify customers with high historical value but lower recent activity.
* Understand revenue concentration across customer segments.
* Develop targeted strategies for each segment.
* Estimate the potential financial impact of customer reactivation.

---

## 2. Dataset

The analysis uses the **Online Retail II** dataset, containing transaction records from a UK-based online retailer between **December 2009 and December 2011**.

Key attributes include:

* Customer ID
* Invoice
* Invoice Date
* Stock Code
* Description
* Quantity
* Unit Price
* Country

### Data Source

[Kaggle — Online Retail II Dataset](https://www.kaggle.com/datasets/tunguz/online-retail-ii/data)

---

## 3. Methodology

The project follows the following analytical workflow:

```text
Raw Data
    ↓
Data Cleaning
    ↓
Exploratory Data Analysis
    ↓
RFM Analysis
    ↓
Feature Preparation
    ↓
K-Means Clustering
    ↓
Customer Segmentation
    ↓
Business Analysis
    ↓
Financial Impact Analysis
    ↓
Power BI Dashboard
```

### RFM Analysis

Customers are evaluated using:

* **Recency:** Days since the customer's most recent purchase.
* **Frequency:** Number of purchases made by the customer.
* **Monetary:** Total amount spent by the customer.

### Customer Segmentation

K-Means clustering is applied to the prepared RFM features. The number of clusters is evaluated using the **Elbow Method** and **Silhouette Score**.

The resulting clusters are interpreted based on their behavioral characteristics and assigned business-oriented segment names.

---

## 4. Key Findings

The final customer-level analysis identified **4,335 customers** across three actionable segments:

| Segment             | Customers | % of Customers | % of Revenue |
| ------------------- | --------: | -------------: | -----------: |
| Low Value Customers |     2,370 |          54.7% |        11.8% |
| Champions           |     1,494 |          34.5% |        54.8% |
| Sleeping Giants     |       471 |          10.9% |        33.4% |

### Main Insights

* **Champions** represent 34.5% of customers but generate **54.8% of total revenue**, making retention a key priority.
* **Sleeping Giants** represent only 10.9% of customers but generate **33.4% of total revenue** and have the highest average historical monetary value.
* **Champions and Sleeping Giants together account for 88.2% of total revenue while representing only 45.4% of customers.**
* A **10% reactivation scenario** for Sleeping Giants represents approximately **$292,078 in potential revenue recovery**.

---

## 5. Business Recommendations

| Segment                 | Strategy            | Objective                                                |
| ----------------------- | ------------------- | -------------------------------------------------------- |
| **Champions**           | Protect & Retain    | Maintain loyalty and reduce customer loss                |
| **Sleeping Giants**     | Reactivate          | Recover potential revenue through targeted campaigns     |
| **Low Value Customers** | Develop Efficiently | Increase frequency and customer value at controlled cost |

### Strategic Prioritization

**1. Protect Champions**
Use loyalty rewards, exclusive benefits, personalized recommendations, and premium experiences.

**2. Reactivate Sleeping Giants**
Use personalized win-back campaigns based on previous purchasing behavior and relevant products.

**3. Develop Low Value Customers Efficiently**
Use automated, lower-cost promotions and cross-selling strategies to increase purchase frequency and average order value.

---

## 6. Financial Impact

A scenario analysis was performed to estimate the potential revenue recovery associated with different Sleeping Giants reactivation rates.

The baseline scenario assumes a **10% reactivation rate**:

$$
\text{Potential Revenue Recovery}
=
\text{Sleeping Giants Revenue}
\times
\text{Reactivation Rate}
$$

Under this scenario:

> **10% Reactivation → ~$292K Potential Revenue Recovery**

These values represent **potential revenue recovery scenarios**, not guaranteed revenue. The assumptions should be validated through controlled marketing experiments.

---

## 7. Power BI Dashboard

The Power BI dashboard translates the analysis into an interactive business decision-support tool.

### Dashboard Sections

* **Executive Overview**

  * Customer and revenue KPIs
  * Customer distribution
  * Revenue contribution
* **Customer Segmentation**

  * RFM profiles
  * Segment characteristics
  * Customer-level analysis
* **Customer Strategy**

  * Segment priorities
  * Recommended actions
* **Financial Impact**

  * Reactivation scenarios
  * Potential revenue recovery
  * Interactive scenario analysis

---

## 8. Key Performance Indicators

The following KPIs are recommended for evaluating the effectiveness of the proposed strategies:

* Reactivation Rate
* Repeat Purchase Rate
* Revenue Recovered
* Customer Retention Rate
* Campaign Cost
* Marketing ROI

---

## 9. Limitations

* The analysis is based on historical purchasing behavior.
* RFM does not capture all customer interactions or characteristics.
* K-Means clustering requires selecting the number of clusters.
* K-Means is sensitive to feature scaling and outliers.
* Customer segments represent behavioral patterns rather than confirmed business categories.
* Sleeping Giants represent **potential inactivity**, not confirmed customer churn.
* Revenue recovery estimates are based on hypothetical reactivation scenarios.

---

## 10. Future Improvements

Potential extensions include:

* Churn prediction using supervised machine learning.
* Customer Lifetime Value (CLV) estimation.
* Product-level recommendation analysis.
* Time-based customer behavior analysis.
* Country-level segmentation.
* Alternative clustering algorithms.
* Automated segment assignment for new customers.
* Integration with CRM and marketing systems.

---

## 11. Project Structure

```text
customer-segmentation/
│
├── README.md
│
├── data/
│
├── notebooks/
│   ├── en/
│   │   ├── 01_data_understanding_cleaning.ipynb
│   │   ├── 02_eda.ipynb
│   │   ├── 03_rfm_analysis.ipynb
│   │   ├── 04_kmeans_segmentation.ipynb
│   │   └── 05_business_impact.ipynb
│   │
│   └── es/
│       ├── 01_data_understanding_cleaning.ipynb
│       ├── 02_eda.ipynb
│       ├── 03_rfm_analysis.ipynb
│       ├── 04_kmeans_segmentation.ipynb
│       └── 05_business_impact.ipynb
│
├── powerbi/
│   └── customer_segmentation.pbix
│
└── images/
    └── dashboard.png
```

---

## 12. Tools & Technologies

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Seaborn**
* **Scikit-learn**
* **Jupyter Notebook**
* **Power BI**
* **DAX**

### Analytical Techniques

* Data Cleaning
* Exploratory Data Analysis
* RFM Analysis
* Feature Engineering
* K-Means Clustering
* Customer Segmentation
* Scenario Analysis
* Business KPI Analysis

---

## 13. Project Versions

* 🇬🇧 **[English Version](./notebooks/en/01_data_understanding_cleaning.ipynb)**
* 🇪🇸 **[Versión en Español](./notebooks/es/01_data_understanding_cleaning.ipynb)**
