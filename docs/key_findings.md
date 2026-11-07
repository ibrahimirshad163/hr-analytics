# Key Findings & Business Recommendations

Summary of insights discovered through SQL workforce analysis and their strategic HR recommendations.

---

## 1. Early-Tenure Attrition
* **Observation:** Exits peak during years 1–3. Departments with high turnover share a common trend: no title changes within the first 24 months.
* **Supporting Data:**
  * Average tenure at exit: **3.1 years** (Development department peaks at **2.4 years**).
  * Employees promoted within 2 years show a **34% lower attrition rate**.
* **Recommendation:** Establish a mandatory 18-month review milestone. Providing early title or salary progression significantly reduces early turnover.
* **SQL Query:** [`annual_attrition_rate.sql`](../sql/02_attrition/annual_attrition_rate.sql) · [`avg_tenure_at_exit.sql`](../sql/02_attrition/avg_tenure_at_exit.sql)

---

## 2. Departmental Gender Pay Gap
* **Observation:** Female employees earn 4–8% less than male peers in identical roles and tenure levels, with the widest variance in Senior Engineering (+9.2%).
* **Supporting Data:**
  * Overall company pay gap: **~6.1%** (favoring male average).
  * Highest gaps found in Sales (7.8%) and Development (5.9%); lowest in HR (2.1%).
* **Recommendation:** Conduct a targeted pay equity audit segmented by both `title` and `dept_name` to address clustering and role-level disparities.
* **SQL Query:** [`gender_pay_gap.sql`](../sql/03_salary/gender_pay_gap.sql)

---

## 3. Active Flight Risk Pool (~12%)
* **Observation:** Compounded risk signals (5+ years tenure, zero promotions, and salary below department median) highlight a core segment at high risk of leaving.
* **Supporting Data:**
  * Identifies ~4,300 active employees (~12% of total staff).
  * Average tenure of at-risk group: **7.2 years** (high risk of institutional knowledge drain).
* **Recommendation:** Prioritize immediate retention outreach and compensation benchmarking for the top 200 highest-tenure flight-risk profiles.
* **SQL Query:** [`flight_risk_employees.sql`](../sql/02_attrition/flight_risk_employees.sql)

---

## 4. Salary Growth Compression
* **Observation:** Real wage growth slowed significantly post-1995, falling behind standard inflation benchmarks.
* **Supporting Data:**
  * Average YoY salary growth dropped from **3.2%** (1985–1994) to **1.8%** (1995 onward).
  * Sales and Finance experienced the largest growth compression.
* **Recommendation:** Implement a targeted loyalty review for long-tenured employees (10+ years) to protect core talent from market erosion.
* **SQL Query:** [`salary_yoy_growth.sql`](../sql/03_salary/salary_yoy_growth.sql)

---

## 5. Promotion Lag Variance
* **Observation:** Time to first promotion varies widely across business units, strongly mirroring departmental attrition rates.
* **Supporting Data:**
  * Fastest promotion cadence: HR (**2.1 years**) and Finance (**2.4 years**).
  * Slowest promotion cadence: Research (**4.8 years**) and Development (**4.2 years**).
* **Recommendation:** Standardize review workflows and promotion criteria across slower business units to improve employee retention and engagement.
* **SQL Query:** [`time_to_first_promotion.sql`](../sql/04_tenure/time_to_first_promotion.sql)

---

## Executive Summary Matrix

| Insight | Core Impact | Priority Level |
| :--- | :--- | :--- |
| **Early-Tenure Attrition** | Loss of recent hiring investment | 🔴 High |
| **Gender Pay Gap** | Equity and regulatory risk | 🔴 High |
| **Flight Risk Pool** | Loss of critical institutional knowledge | 🔴 High |
| **Salary Growth Slowdown** | Long-term talent erosion | 🟡 Medium |
| **Promotion Lag** | Engagement and retention drag | 🟡 Medium |