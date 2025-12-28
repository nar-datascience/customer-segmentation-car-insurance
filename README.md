[README-customer-segmentation.md](https://github.com/user-attachments/files/24357938/README-customer-segmentation.md)
# Car Insurance Customer Segmentation

## Project Overview
This project applies unsupervised learning to segment car insurance policyholders into distinct, actionable customer groups. Using demographic, vehicle, and policy-level data, the analysis identifies meaningful customer segments that can inform pricing, retention, risk management, and cross-selling strategies.

The final model segments customers into six distinct clusters, each with clear business interpretations and recommended actions.

---

## Business Problem
Insurance companies manage customers with widely varying risk profiles, vehicle characteristics, and claim behaviors. Treating all policyholders uniformly can lead to inefficient pricing and missed retention opportunities.

The objectives of this project are to:

1. Identify natural customer segments within an insurance portfolio using unsupervised learning
2. Translate those segments into actionable business strategies such as differentiated pricing, retention programs, and upselling opportunities

---

## Data Description

- **Source:** Kaggle - Car Insurance Claim Prediction dataset - https://www.kaggle.com/datasets/ifteshanajnin/carinsuranceclaimprediction-classification
- **Policyholders:** 58,592
- **Original Features:** 44
- **Feature Types:**
  - Demographics: Age, area cluster, population density
  - Vehicle Information: Make, model, fuel type, NCAP rating, safety features
  - Policy Attributes: Tenure, credit limit, number of claims, claim amount
  - Binary Safety Indicators: Airbags, brake assist, power steering, central locking

---

## Methodology

**Data Preprocessing:**

- One-hot encoded categorical variables (expanded to 68+ features)
- Applied Yeo–Johnson transformations to address skewness
- Normalized features using MinMaxScaler
- Reduced dimensionality using PCA, retaining 15 components and >95% of total variance

**Modeling Approach**
The following models were built:

- K-Means Clustering
- Hierarchical Agglomerative Clustering
- DBSCAN 

The models were evaluated on the following criteria:

- Silhouette Score
- Davies–Bouldin Index
- Calinski–Harabasz Score
- Computational efficiency and scalability

K-Means was selected as the final model based on overall performance and scalability. It had the following metrics:

- Number of clusters: 6
- Silhouette Score: 0.564
- Davies–Bouldin Index: 0.954
- Calinski–Harabasz Score: 44,200

---

## CLuster Results and Recommendations
**Identified Clusters**

1. Small City Drivers with Modern Cars
    - Stable, safety-conscious customers
    - Retain with loyalty discounts or bundled coverage

2. New Customers with Unsafe Cars
    - High risk, short tenure, churn-prone
    - Apply higher base rates for lower-safety vehicles

3. Drivers with the Safest and Largest Cars
    - Premium, low-risk customers
    - Target for loyalty programs and upselling

4. Drivers with Basic, Manual, Diesel Cars
    - Middle-market, budget-conscious
    - Ideal for retention campaigns

5. Reliable Customers in Small Cities with Basic Cars
    - Longest tenure, stable income
    - Offer renewal-based loyalty incentives

6. Big City Drivers with Basic, Modern Cars
    - Low-risk and profitable at scale
    - Cross-sell add-ons (e.g., theft protection, zero depreciation)

Cluster sizes ranged from 4.1% to 32.6% of the portfolio.

---

## Key Insights

- Customer location and policy tenure are the strongest drivers of segmentation
- Safety features and vehicle type strongly influence risk profiles
- Unsupervised learning reveals clear, interpretable customer groups without relying on claim labels

---

## Tools & Technologies
- **Python**
- **pandas**, **NumPy** – data manipulation  
- **matplotlib**, **seaborn** – visualization  
- **scikit-learn** – clustering & dimensionality reduction
- **Jupyter Notebook** – analysis and documentation  

---

## Repository Structure
```
├── Data - Car Insurance Claim Prediction - Kaggle
├── Car Insurance Customer Segmentation Report.pdf
├── Car Insurance Customer Segmentation.ipynb
├── README.md
```

---

## Next Steps
- Incorporate behavioral data (payment history, renewals)
- Track cluster migration over time to monitor risk evolution

---

## Contact
If you’d like to discuss this project or explore related work, feel free to connect with me on LinkedIn or view my other repositories.

