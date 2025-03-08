# Customer Segmentation using Clustering

## Project Overview
This project focuses on customer segmentation based on transactional and demographic data. The goal is to identify distinct customer groups using clustering techniques and analyze their coupon usage behavior. The findings can help optimize marketing strategies and personalize customer incentives.

## Dataset
The project utilizes an Excel dataset containing:
- **Customers**: Demographic details like gender and city.
- **Genders**: Mapping of gender IDs to gender names.
- **Cities**: Mapping of city IDs to city names.
- **Transactions**: Transaction history, including coupon usage status.

## Data Processing & Feature Engineering
1. **Data Loading**: The datasets are loaded from an Excel file and merged appropriately.
2. **Feature Engineering**:
   - Coupon usage frequency per customer is computed.
   - Categorical data (gender and city) is encoded numerically.
3. **Data Scaling**: Features are standardized using `StandardScaler` to improve clustering performance.

## Clustering Approaches
### K-Means Clustering
- K-Means is applied with varying cluster sizes (k=2 to k=9).
- **Evaluation Metrics**:
  - **Elbow Method**: Used to determine the optimal number of clusters based on inertia.
  - **Silhouette Score**: Measures the cohesion and separation of clusters.
- The best k-value is selected based on the highest silhouette score.
- Customers are assigned to clusters, and cluster distributions are analyzed.

### DBSCAN Clustering
- Density-based spatial clustering is applied to detect arbitrary-shaped clusters and noise points.
- **Parameters**:
  - `eps=0.5`: Maximum distance between points in a cluster.
  - `min_samples=5`: Minimum points required to form a cluster.
- Customer segmentation results are visualized, and the cluster distribution is examined.

## Key Findings
- K-Means clustering successfully segments customers based on coupon usage and demographic attributes.
- The **Elbow Method and Silhouette Score** help determine the optimal number of clusters.
- DBSCAN reveals outliers and noise points that K-Means may not capture effectively.
- Cluster analysis provides insights into customer behaviors, such as high vs. low coupon usage groups.

## Visualizations
- **Elbow Method & Silhouette Score Plots**: Determine the optimal k for K-Means.
- **Boxplots of Coupon Usage per Cluster**: Show distribution differences.
- **DBSCAN Cluster Scatter Plot**: Visualizes detected clusters and noise points.

## Output
- The final segmented customer data is saved as `customer_segments.csv`.

## Future Work
- Include additional features like transaction amounts and frequency for more detailed segmentation.
- Experiment with hierarchical clustering and Gaussian Mixture Models (GMM).
- Improve DBSCAN parameter tuning for better noise handling.

## Running the Code
1. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`
2. Place `E-commerce_data.xlsx` in the working directory.
3. Execute the script to generate clusters and visualizations.
4. The final segmented data is saved in `customer_segments.csv`.

---
This project provides valuable customer insights that can drive personalized marketing strategies and improve engagement through targeted promotions.

