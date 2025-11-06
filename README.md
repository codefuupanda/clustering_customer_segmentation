# Customer Segmentation (Clustering)

This project performs customer segmentation on an online retail dataset. Instead of predicting anything, the goal is to group customers into meaningful clusters based on their behavior. This is classic unsupervised learning for marketing and CRM insights.

## Dataset
The dataset (`OnlineRetail.csv`) contains individual purchase records. I aggregate those into customer-level behavior metrics.

## Features Created (RFM Style)
We summarize each customer using:
- **Frequency** – how many orders they placed
- **Monetary** – how much money they spent in total
- **Recency** – how long it has been since their last purchase

These features describe **customer engagement and value**.

## Clustering
We applied:
- **K-Means** clustering with various `k` values
- **Elbow Method** to inspect where improvement levels off
- **Silhouette Score** to evaluate cluster separation quality

We selected the optimal number of clusters based on both heuristics and scoring results.

## What the Clusters Represent

| Cluster | Behavior Pattern | Business Interpretation | Suggested Action |
|--------|-----------------|------------------------|----------------|
| **Cluster 0** | High Frequency + High Spend + Recent Activity | Loyal, valuable customers | Offer rewards, VIP perks, early access |
| **Cluster 1** | Low Frequency + Low Spend + High Recency | At-risk / churned customers | Send re-engagement emails, targeted promos |
| **Cluster 2** | Medium Spend + Irregular Purchases | Occasional / casual customers | Personalized recommendations, seasonal nudges |

This turns unsupervised clusters into **practical customer segments** that support decision-making.

## Why This Matters
Understanding customer segments helps tailor:
- Marketing campaigns
- Retention strategies
- Loyalty programs
- Product recommendations

It turns raw transaction logs into actionable business insight.

---

## Possible Improvements (Next Steps)

- **Scale the Features More Carefully**  
  Trying `StandardScaler` or `RobustScaler` may improve clustering shape when dealing with outliers.

- **maybe additional Clustering Methods**  
  Beyond K-Means:
  - DBSCAN (finds dense customer groups)
  - Agglomerative Clustering (hierarchical tree)
  - Gaussian Mixture Models (soft cluster probabilities)

- **Evaluate Clusters with More Metrics**  
  In addition to Silhouette Score:
  - Calinski-Harabasz Index
  - Davies-Bouldin Score

- **maybe a Visual Cluster Map**  
  Reduce from 3D+ features to 2D using **PCA** or **t-SNE** and plot clusters to understand structure visually.

- **Improve Cluster Naming**  
  Use averages per cluster to assign business-friendly segment names, e.g.:
  - "Champions"
  - "Potential Loyalists"
  - "Needs Attention"
  - "At Risk"

- **Turn Insights into Strategy**  
  Expand from “who they are” to **what to do** with them:
  - Retention campaigns for loyal customers
  - Win-back messages for churned customers
  - Personalized product suggestions for mid-value shoppers

The possible improvements would strengthen both the **analytical depth** and **business value** of the segmentation.
