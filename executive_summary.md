# Executive Summary — RetailGlobe Customer Segmentation  
**Prepared for:** Emma Watson, Marketing Director, RetailGlobe Ltd.  
**Date:** June 2026 | **Dataset:** 133,907 transactions → 124,516 clean transactions · 3,994 customers · Dec 2010 – Dec 2011  

---

## The Problem Solved

RetailGlobe has been treating all customers the same — sending identical emails, promotions, and discounts regardless of customer value or behaviour. This is inefficient: high-value customers may feel undervalued, while low-value or inactive customers receive unnecessary marketing spend.

To address this, we analysed one year of transaction data and grouped customers using **RFM analysis (Recency, Frequency, Monetary value)** combined with **K-Means clustering**. We then validated whether these segments are statistically meaningful using **ANOVA tests** and **R² explanatory power analysis**.

The results show that customer behaviour is not random across segments:

- **ANOVA results show extremely strong statistical separation (p < 0.001 across all metrics)**  
- Segment membership explains:
  - **84.8% of variation in spend (R² = 0.848)**
  - **88.9% of variation in order frequency (R² = 0.889)**
  - **81.1% of variation in recency (R² = 0.811)**  

**Conclusion:** These segments are not arbitrary — they represent real, behaviorally distinct customer groups that are reliable enough for business action.

---

## Top 3 Insights

### 1. Champions drive disproportionate value despite being a small group
Champions represent only **3.7% of customers (147 customers)** but generate extremely high value:

- Average spend: **£1,815.70**
- Average orders: **59.8**
- Very recent activity: **2.7 days since last purchase**
- Revenue share: **20.1%**

This means a very small group of customers contributes a disproportionately large share of revenue. Losing even a few Champions would have immediate financial impact.

---

### 2. The majority of customers are inactive or disengaged
The largest segment is **At-Risk customers (61.1%)**, followed by Lost/Hibernating customers.

- At-Risk: **2,440 customers**
  - Moderate spend (£176.40)
  - Low frequency (6.1 orders)
  - ~30 days since last purchase

- Lost/Hibernating: **531 customers (13.3%)**
  - Extremely low engagement
  - ~228 days since last purchase

Together, this shows that **over 74% of customers are not actively engaged**, representing a major retention opportunity.

---

### 3. Demand is stable but concentrated in specific customer behaviour patterns
Behavioural patterns are highly structured rather than random:

- High-frequency customers drive most revenue stability
- Low-frequency customers are extremely price- or event-driven
- Purchase behaviour is predictable enough that segmentation explains most variance (supported by high R² values)

This confirms that **customer behaviour can be effectively targeted rather than treated uniformly**.

---

## Answering the Key Business Questions

### 1. Who are our VIP customers that we should never lose?

**Champions (147 customers, 3.7%)**

These customers:
- Buy very frequently (59.8 orders on average)
- Spend the most (£1,815 per customer)
- Purchase extremely recently (2.7 days ago)

-> These customers are your **core revenue engine**  
-> Losing even a small percentage would significantly impact total revenue  

---

### 2. Which customers are at risk of leaving us?

**At-Risk customers (2,440 customers, 61.1%)**

These customers:
- Have bought before but are slowing down
- Show declining engagement (30 days since last purchase)
- Still generate meaningful revenue (32.5% share)

-> These are your **highest recovery opportunity group**  
-> Small interventions (discounts, reminders) can produce strong ROI  

---

### 3. How should we segment our base for marketing campaigns?

- **Champions (3.7%)** → Retain & reward  
  VIP access, exclusivity, early product drops  

- **Loyal Customers (21.9%)** → Upsell & maintain  
  Bundles, cross-sell, personalised recommendations  

- **At-Risk (61.1%)** → Win-back campaigns  
  Discount offers, reminders, reactivation emails  

- **Lost / Hibernating (13.3%)** → Low-cost reactivation  
  Seasonal campaigns only, minimal marketing spend  

---

## Customer Segments

| Segment | Customers | Share of Customers (%) | Avg. Spend (£) | Avg. Orders | Last Purchase (avg days) | Revenue Share (%) |
|----------|-----------|------------------------|----------------|-------------|--------------------------|-------------------|
| Loyal Customers | 876 | 21.9% | £687.7 | 22.1 | 8.4 | 45.4% |
| At-Risk | 2,440 | 61.1% | £176.4 | 6.1 | 30.2 | 32.5% |
| Champions | 147 | 3.7% | £1,815.7 | 59.8 | 2.7 | 20.1% |
| Lost / Hibernating | 531 | 13.3% | £49.5 | 1.5 | 228.3 | 2.0% |

---

## Data Reliability & Bias Assessment

### 1. Sampling Bias (UK dominance)
- **87.8% of transactions come from the United Kingdom**
- Other countries (France, Germany, EIRE) are much smaller in volume

-> This introduces **geographical bias**, meaning:
- Insights are heavily UK-driven
- International customers may behave differently
- Global generalisation is limited

---

### 2. Data Cleaning Impact
- Original rows: **133,907**
- Clean rows: **124,516**
- Removed: **9,391 (7.0%)**
  - Missing Customer IDs: 5%
  - Negative quantities (returns/cancellations)

-> This improves data quality but removes:
- Some anonymous transactions that may include valuable customers

---

### 3. Time Window Bias
- Dataset covers **13 months only**
- Strong seasonality (especially Nov–Dec peaks)

-> Risk:
- Seasonal buyers may appear inactive
- Recency is biased against yearly/holiday shoppers

---

### 4. What this analysis does NOT tell us

- It does not explain **why customers stop buying**
  (price, competition, product issues, service quality are unknown)

- It does not include **customer demographics**
  (no age, income, or business type information)

- It does not measure **marketing exposure**
  (we cannot see who received which campaigns)

- It does not capture **external market effects**
  (economic shifts, competitor actions, supply chain issues)

---

## Statistical Validation (Why this segmentation is trustworthy)

### ANOVA Results
All segments are statistically different:

- Monetary: **p < 0.001**
- Frequency: **p < 0.001**
- Recency: **p < 0.001**

-> Interpretation: differences between groups are not due to chance.

---

### R² Explanatory Power

- Spend: **84.8% explained**
- Frequency: **88.9% explained**
- Recency: **81.1% explained**

-> Interpretation:
Segment membership is a strong predictor of customer behaviour.

---

## Final Conclusion

RetailGlobe’s customer base is highly structured, not random. A small group of Champions drives a disproportionate share of revenue, while the majority of customers are either disengaged or at risk of churn.

This segmentation is:
- Statistically valid (ANOVA)
- Highly predictive (R² values)
- Operationally actionable (clear customer groups)

**Recommendation:** Shift from blanket marketing to segment-based targeting immediately to improve retention, increase revenue efficiency, and reduce wasted marketing spend.