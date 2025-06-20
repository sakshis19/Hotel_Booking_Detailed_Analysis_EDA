
## 🏨 Uncovering Patterns in Hotel Booking Data for Operational Efficiency and Revenue Growth  
**Prepared by:** Sakshi Shastri  
**Date:** 08/06/2025  

---

## 🧾 Executive Summary

This case study dives deep into a real-world dataset of hotel bookings to uncover valuable patterns that can help increase revenue and improve operational decisions.  
Think like a hotel manager — you want to know who books your hotel, when, how long they stay, and what influences how much they pay.

We analyzed:
- How early or late guests book (Lead Time)
- Which countries guests come from
- Room upgrades and reassignments
- Duration of stay
- What affects pricing (ADR – Average Daily Rate)

All of this was done using Python, with help from libraries like Pandas, Seaborn, and Matplotlib. The goal is to support data-driven strategies in the hospitality industry.

---

## 📚 Table of Contents
1. [Introduction](#1-introduction)  
2. [Background / Context](#2-background--context)  
3. [Analysis](#3-analysis)  
4. [Conclusion](#4-conclusion)

---

## 1. Introduction

We started with a rich dataset containing over 100,000 rows — each representing a hotel booking. It includes:
- Booking and stay details (e.g., dates, room type, number of guests)
- Guest information (e.g., nationality, whether they are repeat guests)
- Revenue-related info (e.g., ADR, deposit type)

**Why this matters:** These insights help hotels improve customer targeting, optimize pricing, and reduce cancellations.

---

## 2. Background / Context

The dataset includes bookings from two types of hotels:
- 🏙️ City Hotel
- 🌴 Resort Hotel

Challenges in raw data:
- ❌ Missing values (e.g., in "company", "agent", "children")
- 🧩 Date parts were stored in separate columns (day, month, year)

**How we handled it:**
- Cleaned missing values thoughtfully
- Combined date columns into one for better time series analysis

---

## 3. Analysis

### 🔹 Univariate Analysis (Single Variable at a Time)

Helps us understand basic distributions and trends.

- Most bookings happen **0–20 days before check-in**
- Room types A and D are the most booked
- ADR (Average Daily Rate) mostly lies between **50–150**, with a peak near 100

**Visuals used:**
- Bar charts for categorical columns
- Histograms for continuous columns

### 🔸 Bivariate/Multivariate Analysis (Comparing 2+ Variables)

We explored relationships like:
- Do repeat guests pay more?
- Does lead time affect cancellations?
- Do guests from certain countries spend more?

**Key insights:**
- Guests who are repeat customers or book via corporate channels **tend to pay more**
- **Room reassignment** usually correlates with fewer cancellations
- Some booking channels result in lower prices (e.g., agent bookings)

**Boxplots and grouped bar charts** helped bring these patterns to light.

### 📈 Time Series Analysis (Trends Over Time)

- July & August = 🔥 Peak booking months
- Mondays have the most bookings — possibly people plan trips after weekends
- Over time, both hotels show growing volume → 📈 Business expansion

### 🔗 Correlation

We used correlation heatmaps to find relationships between variables.

**Example:**
- `adr` (price per night) and `total_special_requests` have a weak positive relationship → people who pay more often ask for more services

### 🧪 Hypothesis Testing

We asked statistical questions like:
- Do guests who book earlier cancel less often?
- Do repeated guests pay more than first-timers?

And used **t-tests and chi-square tests** to confirm or reject those hypotheses.

### 🧹 Data Cleaning Summary

| Column     | Action                     |
|------------|----------------------------|
| company    | Dropped (too many NaNs)    |
| agent      | Filled with most common ID |
| country    | Filled with top occurring  |
| children   | Filled with 0 or mode      |

---

## ✅ Conclusion

By analyzing this dataset, we learned:
- **Lead time** and **customer type** are strong indicators of pricing and cancellation behavior
- Guests from countries like **UK & France** tend to book earlier and stay longer
- **Transient guests** bring high revenue despite shorter stays
- Room upgrades, booking channels, and deposit types impact **booking reliability**
- Seasonal trends (summer peaks, Monday surges) help optimize marketing & operations

**Business Value:** These insights can help hotels with staffing, pricing, inventory, and customer satisfaction planning.

---

## 🛠 Tools Used

- Python (Pandas, Seaborn, Matplotlib, SciPy)
- Jupyter Notebook
- Excel (initial review)

---

## 📂 Folder Structure

```
hotel-booking-case-study/
├── 61_Sakshi_Shastri_EDA_.ipynb     # Notebook with full analysis
├── dataset/                         # Raw and cleaned data files
├── visualizations/                  # Graphs and plots
└── README.md                        # Project overview
```

---

## 🔗 Connect with Me

📩 LinkedIn: https://www.linkedin.com/in/sakshi-shastri19/
📧 Email: sakshishastri72@gmail.com

Thanks for reading!
