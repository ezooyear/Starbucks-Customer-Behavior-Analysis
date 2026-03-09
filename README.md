# Starbucks Customer Behavior Analysis

## Project Overview

Starbucks frequently uses promotional campaigns such as BOGO (Buy One Get One) and Discount offers to increase customer engagement and purchases. However, customers respond differently to these promotions.

The objective of this project is to analyze customer behavior using the Starbucks Rewards dataset and identify how different customers respond to promotional offers.

This project aims to answer the following questions:

- Which customers are most responsive to promotions?
- Are there customers who purchase regardless of promotions?
- How do demographic characteristics influence promotion preferences?
- How quickly do customers respond to promotional campaigns?

Through these analyses, we aim to derive actionable marketing insights for customer segmentation and promotion strategies.

---

## Dataset

The Starbucks Rewards dataset consists of three tables.

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
| duration | Offer duration |

Offer types include:

- BOGO
- Discount
- Informational

---

### Transcript
Customer activity log.

| Column | Description |
|------|-------------|
| event | Event type |
| person | Customer ID |
| time | Timestamp |
| value | Event details |

Event types include:

- offer received
- offer viewed
- offer completed
- transaction

---

# Data Processing

The `value` column in the transcript dataset contains nested information such as offer ID and transaction amount. Therefore, preprocessing was required to extract structured features.

Processing steps:

- Extract offer_id from value column
- Extract transaction amount
- Standardize event records
- Aggregate customer-level behavior metrics

---

# Feature Engineering

To analyze customer behavior, customer-level features were generated.

Key behavioral features:

- offer_received
- offer_viewed
- offer_completed
- transaction_count
- total_spending
- response_rate
- view_rate
- membership_age
- loyalty_score
- purchase_frequency

These features allow behavioral analysis at the customer level.

---

# Exploratory Data Analysis

EDA was performed to understand customer characteristics and promotion engagement.

Key analyses include:

- Customer demographic distribution
- Promotion completion rate by offer type
- Relationship between promotion engagement and spending
- Reward level impact on completion rate

---

# Customer Segmentation

Based on behavioral features, customers were segmented into three major groups.

### Promotion-sensitive Customers

Customers who actively respond to promotional campaigns.

Characteristics:

- High promotion completion rate
- Promotion-driven purchases

---

### Loyal Customers

Customers who frequently purchase regardless of promotions.

Characteristics:

- High transaction frequency
- Consistent spending

---

### Passive Customers

Customers with low engagement and purchase activity.

Characteristics:

- Low promotion response
- Low transaction count

---

# Promotion Preference by Age Group

Promotion response patterns were further analyzed by age group.

Findings include:

- Younger customers tend to respond more to discount offers.
- Middle-aged customers show higher completion rates for BOGO offers.
- Informational offers show the lowest engagement across all age groups.

This suggests that promotion strategies may benefit from demographic targeting.

---

# Campaign Response Time Analysis

Customer response behavior was analyzed by measuring the time difference between promotional events.

Event flow:

offer received → offer viewed → offer completed

Findings:

- Many customers view promotions shortly after receiving them.
- Customers who complete offers tend to respond quickly after viewing.
- Delayed responses are associated with lower completion probability.

Understanding response timing can help optimize campaign scheduling.

---

# Key Insights

The analysis revealed several key insights:

- BOGO offers demonstrate the highest completion rate among promotions.
- Promotion engagement is positively associated with customer spending.
- Customer behavior patterns can be categorized into promotion-driven, loyalty-driven, and low-engagement groups.
- Promotion preference varies across age groups.
- Faster campaign responses are associated with higher completion rates.

---

# Business Implications

Based on the findings, the following strategies can be suggested.

Promotion-sensitive customers

- Increase targeted discount and BOGO campaigns

Loyal customers

- Provide exclusive loyalty programs and VIP benefits

Passive customers

- Introduce re-engagement campaigns and personalized coupons

Age-based targeting

- Younger customers → discount campaigns
- Middle-aged customers → BOGO promotions

---

# Limitations

This analysis has several limitations.

- Lack of product-level purchase data
- No store location information
- Limited observation window for customer behavior

Future work could include additional customer interaction data and more advanced customer lifetime value modeling.

---

# Tech Stack

Python  
Pandas  
Matplotlib  
Seaborn
