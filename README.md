# Telco Customer Churn Analysis
This project analyses customer churn in a telecom dataset using Python, Pandas, Seaborn and Matplotlib.   The goal is to understand which customer segments are most at risk of churn and translate those findings into concrete business recommendations.


## __Business / Sponsor Context and Objective__

- A subscription-based telecom operator is seeing elevated churn, especially among month-to-month and high-bill customers. Losing these customers directly erodes recurring revenue and increases acquisition spend.

- In this project, I take the role of a junior data analyst supporting the commercial and customer success teams to:

   - Build a clear churn funnel from “active” to “churned”.

   - Quantify which segments are driving churn (e.g. contract type, tenure, internet service, charges).

   - Translate patterns into practical retention actions (pricing, bundles, support, and onboarding).


## __Dataset__ 

- Source: Public “Telco Customer Churn” dataset from Kaggle.

- Rows: 7,043 customers

- Target variable: Churn (Yes / No)

Logical entities and fields:

- Customers

    - customerID, gender, SeniorCitizen, Partner, Dependents, tenure

- Services

    - PhoneService, MultipleLines

    - InternetService (DSL, Fiber optic, None)

    - OnlineSecurity, OnlineBackup, DeviceProtection, TechSupport

    - StreamingTV, StreamingMovies

- Contracts & Billing

    - Contract (Month-to-month, One year, Two year)

    - PaperlessBilling, PaymentMethod

- Financials

    - MonthlyCharges, TotalCharges

Repository contents

- data/churn_data.csv – raw dataset from Kaggle

- notebooks/telco_customerchrun.ipynb – EDA, churn funnel analysis and plots

- reports/TCA_Executive Summary.pdf – stakeholder-facing summary and recommendations

- images/ – optional: charts and ERD screenshots for the README



## __Insights Summary__

- Overall churn is around 26–27%, meaning roughly 1 in 4 customers leave.

- Month-to-month contracts have churn above 40%, versus low churn in 1–2 year contracts.

- High MonthlyCharges customers are significantly more likely to churn, especially on Fiber optic plans.

- Customers without OnlineSecurity or TechSupport show higher churn, suggesting that perceived protection and support are strong retention levers.

- Paperless billing and some payment methods are associated with more churn, pointing to a more digital, price-sensitive customer group.

  

  ## __Churn Funnel Metrics__


Stage 1 – Active base

   - All currently active customers at a point in time.

Stage 2 – At-risk customers

   - Active customers who match risk patterns:

      - Month-to-month contract

      - High MonthlyCharges

      - Fiber optic internet

      - No security/support add-ons

Stage 3 – Churn events

  - Customers with Churn = "Yes".

From this, follwoing were derived:

- Stage counts: Active, At-risk, Churned.

- Conversion / drop-off:

     - Active → At-risk (% of base in high-risk profile).

     - At-risk → Churned (% of at-risk who actually churn).

- Value at risk: Sum of MonthlyCharges or approximate annualised revenue for each stage.

 

## __Funnel Subsections__

1. Overall churn funnel

- Visualises the split between retained vs churned customers.

- Highlights that a small number of driver features explain a large share of churn (contract type, internet service, price).

2. “Eligible → At-risk → Churned” (Risk segmentation)

Analogous to an eligible→consented funnel in trials, here:

- Eligible: All active customers.

- At-risk: Customers matching a simple risk rule set, such as:

    - Month-to-month

    - MonthlyCharges in top quartile

    - Fiber optic

    - No OnlineSecurity or TechSupport

- Churned: Those at-risk who actually leave.

__Key questions answered:__

- What percentage of the base is at-risk?

- How much revenue is concentrated in at-risk segments?

- Which risk rules are most predictive (e.g. contract vs price vs service type)?

3. Timing / Lifecycle (Tenure-based risk)

Using tenure as a proxy for lifecycle stage:

- Early tenure customers (e.g. 0–6 months) often have higher churn – a critical onboarding period.

- Churn tends to decline with tenure, indicating that once customers make it past the early phase, they are more likely to stay.

- This supports designing early-life retention journeys.

  

 ## __Recommendations__

Translating the analysis into operations and commercial actions:

1. Lock in high-risk month-to-month customers

- Prioritise outreach to month-to-month, high-bill, fiber customers.

- Offer contract upgrades, loyalty discounts or bundled benefits to reduce immediate churn risk.

2. Design early-life onboarding programmes

For customers in their first 3–6 months, ensure:

- Proactive service quality checks.

- Education on key features and self-service options.

- Targeted offers for OnlineSecurity and TechSupport.

3. Revisit pricing and value communication for fiber plans

- Review price positioning for high-charge fiber plans.

- Emphasise value beyond speed: stability, security and support.

4. Use a simple churn risk score in CRM

- Convert the risk rules into a churn flag or score.

- Surface this in CRM so sales, retention and support teams can prioritise outreach.

5. Monitor KPIs in a live churn dashboard

- Overall churn rate and trend

- Churn by contract type, tenure band, service type and charge band

- Revenue at risk and revenue saved by retention campaigns

  

  ## __Attachments__
  - notebooks/telco_customerchrun.ipynb
  - Executive Summary Document
  
  
