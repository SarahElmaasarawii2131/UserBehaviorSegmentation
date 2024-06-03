# UserBehaviorSegmentation
Repository dedicated to analyzing user interaction data from various social media platforms including Facebook, Instagram, Pinterest, and LinkedIn.
# Social Media User Segmentation Project

## Introduction

Welcome to the Social Media User Segmentation Project! This project aims to analyze user interactions data from various social media platforms, including Facebook, Instagram, Pinterest, and LinkedIn, to segment users based on their activity patterns. By leveraging clustering techniques, we strive to identify distinct user groups and extract insights to facilitate targeted marketing strategies, enhance user engagement, and improve satisfaction.

## Dataset Description

The dataset used for this project is the Netmob Dataset, collected in Paris over a span of 4 days from 16th to 19th March 2019. It includes user interaction data from Facebook, Instagram, LinkedIn, and Pinterest, with data collected every 15 minutes.

## Workflow

1. **Preprocessing & Aggregation:**
   - Combined data of 4 days for each platform.
   - Aggregated data by TileID, using median values.
   - Filtered out noisy or irrelevant data using a city geojson file.
   - Aggregated user interactions in 15-minute intervals.
   - Verified file existence, removed duplicates, & ensured data completeness.

2. **Clustering Methods:**
   - **K-Means:** Simple and fast for large datasets, assumes well-separated and spherical clusters.
   - **Gaussian Mixture Model (GMM):** Can model clusters of arbitrary shapes and sizes, accounts for the covariance structure of the data.

3. **Clustering Results:**
   - Conducted clustering for each platform using both K-Means and GMM.
   - Compared the performance of both methods using Silhouette Scores.

## Results

### Clustering Comparison

| Platform   | K-Means Silhouette Score | GMM Silhouette Score |
|------------|---------------------------|----------------------|
| Facebook   | 0.584                     | 0.216                |
| Instagram  | 0.570                     | 0.072                |
| Pinterest  | 0.302                     | 0.030                |
| LinkedIn   | 0.627                     | 0.190                |

## Conclusion

The findings underscore the importance of selecting the appropriate clustering algorithm to accurately understand user behavior. Key conclusions include:

- **K-Means Superiority:** K-Means consistently outperformed GMM, indicating its robustness and suitability for clustering social media data.
- **Platform Variability:** Instagram demonstrated well-defined user behaviors, making it suitable for targeted marketing. Pinterest may require further refinement in clustering techniques or additional data preprocessing.

---

For more information, please refer to the detailed documentation and code repository provided. If you have any questions or feedback, feel free to reach out!
