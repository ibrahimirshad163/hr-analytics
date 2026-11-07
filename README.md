# 📊 HR Analytics: Workforce & Salary Intelligence Platform

An end-to-end data analytics portfolio project analyzing workforce demographics, departmental attrition risks, gender pay disparities, and compensation trends using **MySQL** and **Power BI**. 

---

## 🚀 Project Overview
This project investigates an enterprise employee database (~300,000+ records) to uncover structural workforce insights and provide actionable HR recommendations. The solution combines robust relational data modeling in SQL with an interactive Power BI dashboard designed for executive stakeholders.

### Key Objectives
* **Identify Attrition Drivers:** Pinpoint high-risk tenure windows and departmental turnover trends.
* **Audit Compensation & Equity:** Quantify gender pay gaps across roles and evaluate historical wage growth.
* **Evaluate Flight Risk:** Build a multi-signal risk model to flag active employees with high probability of departure.
* **Track Career Progression:** Measure promotion cadences and management pay ratios.

---

## 🛠️ Tech Stack & Architecture
* **Database & Querying:** MySQL (`employees` sample database, 300K+ records, 6 core relational tables).
* **Data Integration:** MySQL Connector/NET, Power Query (M Code).
* **Visualization & BI:** Power BI Desktop (Interactive slicers, cross-filtering, DAX measures).
* **Version Control:** Git & GitHub.

---

## 📊 Dashboard Preview
* **Executive Summary Cards:** Total Headcount (257+ in drill view / 300K+ overall), Average Salary ($65K), Average Tenure, and Female Employee Ratio (34.24%).
* **Interactive Slicers:** Department-level filtering with dynamic visual updates.
* **Visual Breakdown:** Headcount by Department, Top Highest Paid Titles, Gender Split company-wide and department-wide.

*(Add your dashboard screenshots here in your repo: `assets/dashboard_overview.png`)*

---

## 🔍 Key Findings & Business Insights

1. **Early-Tenure Attrition:** Attrition peaks heavily in years 1–3. Employees who receive a title change within their first 24 months exhibit a **34% lower attrition rate**.
2. **Departmental Gender Pay Gap:** Female employees earn 4–8% less on average than male peers in identical roles, with the widest variance in Senior Engineering (+9.2%).
3. **Active Flight Risk Pool:** ~12% of active staff (~4,300 employees) meet multi-signal risk criteria (5+ years tenure, zero promotions, salary below department median).
4. **Salary Growth Compression:** Real wage growth dropped from **3.2%** (1985–1994) to **1.8%** (post-1995), falling behind standard inflation benchmarks.
5. **Promotion Lag Variance:** Average time to promotion ranges from **2.1 years** (HR) to **4.8 years** (Research), strongly correlating with departmental turnover.

---

## 📂 Repository Structure

```text
hr-analytics/
│
├── dashboard/
│   └── HR_Analytics_Dashboard.pbix   # Power BI interactive report
│
├── sql/
│   ├── 01_overview/                  # Workforce overview queries
│   ├── 02_attrition/                 # Attrition & flight risk queries
│   ├── 03_salary/                    # Pay gap & YoY growth queries
│   └── 04_tenure/                    # Promotion & tenure queries
│
├── docs/
│   ├── business_questions.md         # Core analytical questions
│   ├── data_dictionary.md            # Definitions, filters & schema rules
│   └── key_findings.md               # Detailed insights & recommendations
│
└── README.md                         # Project documentation
