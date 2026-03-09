# Starbucks Customer Behavior Analysis

## Project Overview

Starbucks frequently uses promotional campaigns such as BOGO (Buy One Get One) and Discount offers to increase customer engagement and purchases. However, customers respond differently to these promotions.

The objective of this project is to analyze customer behavior using the Starbucks Rewards dataset and identify how different customers respond to promotional offers.

Through this analysis, we aim to answer the following questions:

- Which customers are most responsive to promotions?
- Are there customers who purchase regardless of promotions?
- How can customers be segmented based on their behavioral patterns?

The final goal is to derive actionable marketing insights through customer behavior analysis.

---

## Dataset

This project uses the **Starbucks Rewards Dataset**, which consists of three tables.

### Profile

Customer demographic information.

| Column | Description |
|------|-------------|
| age | Customer age |
| gender | Gender |
| income | Annual income |
| became_member_on | Membership start date |

---

### Portfolio

Information about promotional offers.

| Column | Description |
|------|-------------|
| offer_type | Type of offer |
| reward | Reward value |
| difficulty | Required spending |
| duration | Duration of the offer |

Offer types include:

- BOGO (Buy One Get One)
- Discount
- Informational

---

### Transcript

Customer activity log data.

| Column | Description |
|------|-------------|
| event | Customer event |
| person | Customer ID |
| time | Event timestamp |
| value | Event details |

Event types include:

- offer received
- offer viewed
- offer completed
- transaction

---

## Data Processing

The `value` column in the transcript dataset contains nested information such as:

- offer_id
- transaction amount
- reward

To make the data analyzable, the following preprocessing steps were performed:

- Extract `offer_id`
- Extract transaction `amount`
- Standardize event records

Customer-level behavioral features were then created.

Key features include:

- offer_received
- offer_viewed
- offer_completed
- transaction_count
- total_spending
- response_rate
- view_rate
- membership_age
- loyalty_score

---

## Exploratory Data Analysis

Exploratory analysis was conducted to understand customer characteristics and promotional engagement.

Key analyses include:

- Customer age and income distribution
- Offer completion rate by offer type
- Relationship between promotion engagement and spending
- Reward level and promotion response analysis

---

## Customer Segmentation

Based on behavioral metrics, customers were grouped into three major segments.

### Promotion-sensitive Customers

Customers who frequently respond to promotional offers.

Characteristics:

- High offer completion rate
- Promotion-driven purchases

---

### Loyal Customers

Customers who purchase frequently regardless of promotions.

Characteristics:

- High transaction frequency
- Consistent spending

---

### Passive Customers

Customers with low engagement and low purchase frequency.

Characteristics:

- Low promotion response
- Low transaction count

---

## Key Insights

The analysis revealed several important insights.

- **BOGO offers show the highest completion rate among promotions.**
- Some customers make purchases regardless of promotions, indicating strong brand loyalty.
- Customer behavior patterns can be categorized into promotion-driven, loyalty-driven, and low-engagement groups.

---

## Business Implications

Based on the findings, the following strategies can be suggested.

**Promotion-sensitive customers**

- Increase targeted discount and BOGO campaigns

**Loyal customers**

- Provide loyalty programs and exclusive membership rewards

**Passive customers**

- Offer re-engagement coupons and personalized promotions

---

## Limitations

This analysis has several limitations.

- Lack of product-level purchase information
- No geographic store information
- Limited time span of behavioral data

Future work could incorporate additional customer interaction data for more detailed behavioral modeling.

---

## Tech Stack

Python  
Pandas  
Matplotlib  
Seaborn
