# RFM-Based Customer Segmentation & Retention Analysis on Global Superstore

## Project Background

This project was developed as the final project of the **Machine Learning Bootcamp**, completed collaboratively by a team of three members. The project involved applying data analysis and machine learning techniques to identify customer purchasing patterns, develop meaningful customer segments, and derive business insights to support customer retention and revenue growth strategies.

### Team Members
1. **Rizal Afandi** — M004D5Y1738
2. **Muhammad Aflah Ghozi Susanto** — M004D5Y1199
3. **Ahmad Haydar Alfarizqi** — M004D5Y0095

# 1. Business Understanding

Understanding customer purchasing behavior is essential for businesses to maintain customer relationships, improve retention, and maximize revenue contribution. However, customers do not contribute equally to business performance. Some customers purchase frequently and generate substantial revenue, while others purchase less frequently or have not made a purchase for an extended period.

Without a structured customer segmentation approach, businesses may struggle to identify their most valuable customers, recognize customers with declining engagement, and allocate marketing resources effectively.

This project aims to analyze historical purchasing behavior using the Recency, Frequency, and Monetary (RFM) framework to identify distinct customer segments based on their purchasing patterns and financial contributions.

The analysis focuses on three key business questions:

- **Who are the most valuable customers?** Identify customers who contribute significantly to revenue through frequent purchasing activity and higher spending.
- **Which customers may be at risk of disengagement?** Identify customers with longer periods since their last purchase and relatively low purchasing frequency.
- **How can customer segmentation support business strategies?** Translate customer behavior patterns into opportunities for retention, reactivation, and targeted marketing initiatives.

# 2. Result Summary of the Project

The project analyzed **9,800 transaction records from 793 unique customers** using historical sales data from the Global Superstore dataset.

Customers were segmented into three distinct groups based on their Recency, Frequency, and Monetary values using K-Means clustering.

### Customer Segmentation Results

| Customer Segment | Customers | Customer Share | Revenue Contribution |
|---|---:|---:|---:|
| Regular Customers | 399 | 50.3% | 33.8% |
| At-Risk Customers | 111 | 14.0% | 7.9% |
| High-Value Customers | 283 | 35.7% | 58.3% |
| **Total** | **793** | **100%** | **100%** |

### Key Segment Characteristics

**1. High-Value Customers (Cluster 2)**

- Represent 35.7% of the customer base.
- Generate approximately 58.3% of total customer revenue.
- Have the highest average purchase frequency at 8.85 transactions per customer.
- Generate the highest average monetary value of approximately $4,660 per customer.
- Have an average recency of approximately 79 days.

This segment represents the most valuable customer group, making customer retention and relationship management important to sustaining revenue performance.

**2. Regular Customers (Cluster 0)**

- Represent 50.3% of the customer base.
- Contribute approximately 33.8% of total customer revenue.
- Have an average purchase frequency of 5.02 transactions.
- Generate an average monetary value of approximately $1,913 per customer.
- Have an average recency of approximately 90 days.

This segment represents the largest customer group, offering opportunities to increase purchase frequency and encourage higher spending through targeted engagement and cross-selling initiatives.

**3. At-Risk Customers (Cluster 1)**

- Represent 14.0% of the customer base.
- Contribute approximately 7.9% of total customer revenue.
- Have the longest average recency of approximately 535 days.
- Have the lowest average purchase frequency at 3.73 transactions.
- Generate an average monetary value of approximately $1,616 per customer.

This segment shows signs of declining purchasing engagement, making it a potential target for customer reactivation campaigns and win-back strategies.

The clustering process achieved a **Silhouette Score of 0.383**, providing a moderate indication of separation between the identified customer segments.

# 3. Key Takeaways

- **Revenue is concentrated among high-value customers.** Although they represent only 35.7% of the customer base, this segment contributes approximately 58.3% of total revenue. Maintaining their engagement is therefore important for sustaining business performance.

- **The largest customer segment presents an opportunity for revenue growth.** Regular customers account for more than half of the customer base but contribute approximately 33.8% of revenue. Increasing their purchase frequency and average spending could create additional revenue opportunities.

- **A portion of customers shows signs of disengagement.** The at-risk segment has an average recency of approximately 535 days, indicating a substantial gap since their last recorded purchase. These customers may require targeted reactivation efforts to encourage repeat purchases.

- **Customer segmentation enables more targeted marketing strategies.** Different purchasing behaviors require different engagement approaches. High-value customers may benefit from loyalty initiatives, regular customers from upselling and cross-selling campaigns, and at-risk customers from personalized win-back offers.

- **Customer value should be evaluated beyond transaction volume.** Combining purchase recency, frequency, and monetary contribution provides a more comprehensive understanding of customer relationships than relying on revenue alone.

# 4. Process

- Importing the required Python libraries and loading historical sales transaction data from the Global Superstore dataset.
- Performing data understanding, data inspection, and exploratory analysis to examine sales trends, customer purchasing patterns, product categories, and transaction distributions.
- Conducting data cleaning, date preparation, and customer-level data aggregation to calculate Recency, Frequency, and Monetary (RFM) metrics.
- Applying data scaling and K-Means clustering to group customers based on their purchasing behavior and determine distinct customer segments.
- Evaluating cluster quality using the Silhouette Score and analyzing segment characteristics based on purchasing activity, revenue contribution, product preferences, and customer profiles.
- Translating customer segmentation results into business insights and potential strategies for customer retention, reactivation, and revenue growth.

# 5. Solution Statement

This project provides a data-driven customer segmentation approach to help businesses better understand customer value and purchasing engagement.

By combining Recency, Frequency, and Monetary metrics, the analysis identifies distinct customer groups with different purchasing characteristics and revenue contributions.

The resulting segmentation can serve as a foundation for more targeted customer relationship and marketing strategies, enabling businesses to:

- **Retain High-Value Customers:** Prioritize customer engagement and loyalty initiatives for customers who contribute significantly to revenue.
- **Grow Regular Customers:** Encourage repeat purchases and increase customer spending through relevant product recommendations, cross-selling, and upselling opportunities.
- **Reactivate At-Risk Customers:** Develop targeted win-back campaigns to reconnect with customers who have not made purchases for an extended period.
- **Optimize Marketing Resources:** Allocate marketing efforts based on customer value, purchasing behavior, and engagement levels.
- **Support Revenue Growth:** Use customer-level insights to identify opportunities for improving purchase frequency and long-term customer value.

Ultimately, the objective is to move beyond treating all customers equally toward a more targeted, customer-centric business strategy that prioritizes retention, strengthens customer relationships, and maximizes revenue contribution.
