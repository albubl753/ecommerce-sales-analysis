# E-Commerce Sales & Performance Data Audit

## Business Goal
Perform Exploratory Data Analysis (EDA) on global e-commerce data to evaluate traffic acquisition efficiency, market localization needs, and CRM performance. A secondary objective is to audit data integrity and validate business models using statistical testing.

## Tech Stack
* **Languages & Libraries:** Python (Pandas, Matplotlib, Seaborn, SciPy)
* **Database:** Google BigQuery (SQL)
* **BI Tool:** Tableau Public

## Interactive Dashboard
*[View Interactive E-Commerce Dashboard on Tableau Public](https://public.tableau.com/views/Portfolio1_17779263405390/Dashboard1?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)*

## Key Analytical Findings & Statistical Insights

* **Traffic & Acquisition:** Organic search is the top performer, generating >35% of both traffic and revenue. Desktop devices dominate, accounting for ~60% of sessions and sales. 
* **Market Fit & Localization:** The US is the leading market. Category distribution in the US perfectly mirrors the global trend (holding a 42-46% share per category). This indicates no need for local assortment adaptation; a unified global strategy is sufficient.
* **CRM & Retention Inefficiency:** Registration and email subscriptions do not impact purchasing behavior. An independent t-test (p-value = 0.302) confirmed no statistically significant difference in average order value between guest users ($955.53) and registered users ($928.63). The company has a database of ~28k users but fails to monetize it, highlighting a critical need for alternative retention tools (e.g., push notifications, loyalty programs).

## Data Integrity Audit (Anomaly Detection)
During the EDA, several statistical anomalies were detected, strongly suggesting the dataset has a synthetic/artificial origin:
1. **Perfect Parity:** Session share and revenue share perfectly match across all channels and devices, which contradicts real-world funnel drop-offs.
2. **Unrealistic Linearity:** Pearson correlation between traffic and revenue returned a p-value near 0 with zero local market deviations.
3. **Zero Retention:** 100% of the ~28,000 authorized accounts recorded exactly 1 session over a 3-month period, which is impossible in a functioning e-commerce environment.
