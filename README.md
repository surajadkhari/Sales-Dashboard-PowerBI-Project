# 📊 Power BI Sales Analytics Projects – Dashboard Showcase

Hi! I'm Surat Adhikari – a Data Science student passionate about transforming raw data into meaningful business insights. This project is a showcase of two Power BI dashboards I built using **realistic sales data from a database**, with the aim of demonstrating my growing skills in **data analytics**, **DAX**, **data modeling**, and **AI-powered storytelling** in Power BI.

---

## 💼 Project Overview

This repository highlights my **intermediate to advanced Power BI work** using a sales dataset. The dashboards explore business KPIs such as sales, profit, customer demographics, and trends over time. My goal is to present data in a way that not only informs but helps decision-makers act faster.

---

## 🧠 What I Learned

- How to design clean and informative dashboards using Power BI
- Creating dynamic **DAX measures** like `TOTALYTD`, `LastMonthProfit`, and `MoM%`
- Using **AI visuals** like Smart Narratives and Key Influencers for better storytelling
- Handling **time intelligence** with a custom `DateTable`
- Presenting multi-dimensional insights in a business-friendly format

---

## 🔍 Project Details

### 🛒 **Dashboard: Sales Performance Overview**

<img width="971" alt="Screenshot 2025-04-18 at 7 15 22 PM" src="https://github.com/user-attachments/assets/522b0252-5a82-42cd-9c04-9e233e3e457b" />


#### 🔹 KPIs
- **Total Sales:** 20.22M  
- **Total Cost:** 11.75M  
- **Profit %:** 72.16%

#### 🔹 Visuals Included
- Donut charts for **Customer Age Group** and **Occupation**
- Monthly **Profit Comparison** (bar + line)
- **MoM Growth** visualization across years
- Sub-category wise **Cost/Sales/Profit breakdown**

---

## 📊 Key DAX Measures Used

```DAX
LastYearProfit = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))

LastMonthProfit = CALCULATE([Profit], PREVIOUSMONTH(DateTable[Date]))

MOM% = DIVIDE([Profit] - [LastMonthProfit], [LastMonthProfit], 0)

TOTALYTD = TOTALYTD([Profit], DateTable[Date])

TOTALMTD = TOTALMTD([Profit], DateTable[Date])
