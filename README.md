# SmartCart Customer Clustering System

## Project Overview
SmartCart is a growing e-commerce platform facing a common challenge: treating all customers the same. Without understanding individual behavior patterns, marketing becomes inefficient. 

I developed this **Intelligent Customer Segmentation System** using unsupervised machine learning to group customers based on their demographics, purchasing behavior, and platform engagement. This allows the business to deliver personalized marketing and proactively address churn.

## Key Technical Steps

### 1. Data Preprocessing & Cleaning
* [cite_start]**Missing Values**: Handled missing `Income` data by imputing the median value to maintain dataset integrity[cite: 2].
* [cite_start]**Outlier Removal**: Used visualizations (like pairplots) to identify and remove anomalies that could skew the clustering results[cite: 2].

### 2. Feature Engineering
[cite_start]Created meaningful new attributes to capture deeper customer insights[cite: 2]:
* **Age**: Derived from birth year.
* **Customer Tenure**: Calculated total days since enrollment.
* **Total Spending**: Aggregated spending across all product categories (Wines, Fruits, Meat, Fish, Sweets, and Gold).
* **Total Children**: Combined `Kidhome` and `Teenhome` into a single household metric.
* **Simplified Categories**: Streamlined `Education` and `Marital_Status` into more manageable groups like "Graduate/Postgraduate" and "Living Alone/With Partner."

### 3. Feature Transformation
* [cite_start]**Encoding**: Converted categorical data into numerical format using One-Hot Encoding[cite: 2].
* [cite_start]**Scaling**: Applied `StandardScaler` to ensure all features contribute equally to the distance-based clustering algorithm[cite: 2].

### 4. Dimensionality Reduction (PCA)
With over 15 features, I performed **Principal Component Analysis (PCA)** to reduce the data to 3 dimensions. [cite_start]This minimized noise and allowed for clear 3D visualization of the customer clusters[cite: 2].

### 5. K-Means Clustering
* [cite_start]**Optimization**: Used the **Elbow Method** and **Silhouette Scores** to determine that **K=4** was the optimal number of clusters[cite: 2].
* **Analysis**: Each of the four clusters represents a unique customer persona, ranging from high-spending loyalists to budget-conscious new users.

## Strategic Insights & Results
By analyzing the unique behavior of each cluster, I proposed tailored strategies:
* **High-Value Segments**: Focus on loyalty programs and exclusive previews.
* **Budget-Conscious Segments**: Target with discounts and "value-for-money" campaigns.
* **Churn-Prone Segments**: Implement re-engagement emails based on their specific past interests.

## Technologies Used
* **Language**: Python
* **Libraries**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Tools**: Jupyter Notebook

---
*Developed as part of an AI/ML initiative to support data-driven decision-making at SmartCart.*