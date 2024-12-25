# Exploring Customer Segments Using K-Means Clustering

## Data Preparation

- **Handle Missing Values**: Identify and address any missing or incomplete data entries to ensure a clean dataset.
- **Identify Inconsistencies**: Detect and resolve any discrepancies or outliers in the data that could affect the clustering results.

## Data Transformation

- **Scaling/Normalizing Data**: Apply scaling techniques (e.g., Standardization, Min-Max Scaling) to ensure that all features contribute equally to the clustering model.
- **Feature Engineering**: Create any additional features that may help improve the model's performance or provide better insights. (TotalSpend, Count, SinceYearEnd)

## Data Cleaning

- **Removing Duplicates**: Eliminate any duplicate rows to prevent skewing of results.
- **Fixing Data Types**: Ensure that each feature is of the correct data type (e.g., converting string columns to categorical types if necessary).
- **Handling Outliers**: Investigate and address any extreme values that could distort the clustering.

### Before Filterig Outliers
![outliers](image.png)

### After filtering outliers
![filter_outliers](image-1.png)

### Customer Data after 

| Customer ID | TotalSpend | Counts | LatestDate            | sinceYearEnd |
|-------------|------------|--------|-----------------------|--------------|
| 12346       | 144.02     | 2      | 2010-06-28 13:53:00   | 167          |
| 12347       | 966.87     | 2      | 2010-12-07 14:57:00   | 5            |
| 12348       | 221.16     | 1      | 2010-09-27 14:59:00   | 76           |
| 12349       | 1946.64    | 2      | 2010-10-28 08:23:00   | 45           |
| 12351       | 300.93     | 1      | 2010-11-29 15:23:00   | 13           |


## Data Analysis

- **Exploratory Data Analysis (EDA)**: Visualize and understand the patterns in the data before applying the clustering algorithm.
- **Clustering**: Use K-Means (or another algorithm) to segment the customers based on their behavior and characteristics.
- **Model Evaluation**: Evaluate the clustering results using metrics such as inertia, silhouette score, or visualizations to assess the quality of the clusters.


### 3D plot for feature after scaled

![scaled_3d](image-2.png)

### choosing clusters amount

![cluster_k](image-3.png)

### Pairplot for features

![pairplot](image-4.png)

### Cluster Descriptions

- **Cluster 0**: 
  - **Low Spending**: Customers in this cluster have a relatively low total spend, indicating they are not heavy spenders.
  - **Higher Date Since Last Purchase**: These customers have not made a purchase in a long time, suggesting they may be inactive or have a low engagement level.
  - **Low Counts**: This group tends to have a low frequency of purchases, indicating infrequent buyers.

- **Cluster 1**: 
  - **High Spending**: Customers in this cluster are high spenders, indicating that they tend to make larger purchases.
  - **Recently Active**: These customers have made a purchase recently, suggesting they are actively engaged with the business.
  - **High Purchase Count**: They have a high number of transactions, showing they are frequent buyers.

- **Cluster 2**: 
  - **Higher than Cluster 0**: Customers in this group have higher total spending and purchase frequency than Cluster 0.
  - **Higher Recency**: These customers have made recent purchases, indicating higher engagement compared to Cluster 0.
  - **Overall Active but Less Frequent**: While they may not have as high frequency as Cluster 1, they show a balance between recency, spending, and purchase count.

- **Cluster 3**: 
  - **High Spending**: Like Cluster 1, customers in this cluster are high spenders.
  - **Moderate Purchase Count**: These customers make purchases more moderately compared to Cluster 1 but still at a notable level.
  - **Recently Active**: These customers have made purchases recently, indicating they are fairly engaged, though not as frequently as Cluster 1.

