# Customer Segmentation using K-Means Clustering

This project applies K-Means clustering to the Mall Customers dataset in order to identify distinct customer segments based on purchasing behavior. Customer segmentation is a common technique in marketing analytics, helping organizations to personalize strategies, tailor promotions, and improve customer targeting. The analysis focuses primarily on two features: Annual Income and Spending Score.

## Objective

The aim of this project is to:
- Perform exploratory analysis on customer data  
- Apply the K-Means clustering algorithm  
- Determine an appropriate number of clusters using the WCSS (within-cluster sum of squares) method  
- Visualize distinct groups of customers  
- Demonstrate how clustering can be used for business decision-making  

## Dataset

The dataset used in this project is the **Mall Customers** dataset, which contains the following variables:

- CustomerID  
- Gender  
- Age  
- Annual Income (k$)  
- Spending Score (1–100)  

The analysis is performed using only Annual Income and Spending Score, which are commonly used to understand customer purchasing power and spending behavior.

## Methodology

### 1. Data Loading and Inspection
The data is loaded using `pandas`, and basic exploratory steps include:
- Viewing the first few rows  
- Checking the dataset shape  
- Inspecting data types  
- Identifying missing values  

### 2. Feature Selection
The model uses the following features:
- Annual Income  
- Spending Score  

These columns are extracted into a NumPy array for clustering.

### 3. Choosing the Number of Clusters
The optimal number of clusters is explored using:
- WCSS (within-cluster sum of squares)  
- Iterating through values of k from 1 to 10  

This allows visual inspection of the "elbow point" to select a meaningful number of clusters.

### 4. K-Means Clustering
K-Means is applied with:
- `init='k-means++'` to improve initialization  
- A fixed random state for reproducibility  
- Five clusters identified as an appropriate choice  

Cluster labels are generated for each customer.

### 5. Optional Dimensionality Reduction
Principal Component Analysis (PCA) is included as an optional step to reduce feature dimensionality. Although the clustering itself is performed on the original two features, PCA may be used when extending the project with additional variables.

### 6. Visualization
The final clusters are visualized using scatter plots:
- Each cluster is shown in a distinct color  
- Centroids of all clusters are plotted  
- X-axis: Annual Income  
- Y-axis: Spending Score  

This visualization illustrates how the algorithm groups customers with similar financial and spending characteristics.

## Technologies and Libraries

The following Python libraries are used:
- numpy  
- pandas  
- matplotlib  
- seaborn  
- scikit-learn  

The project is implemented in a standard Python environment and can be executed in Jupyter Notebook, Google Colab, or any Python IDE.

## Running the Project

1. Install necessary libraries:
pip install numpy pandas matplotlib seaborn scikit-learn
2. Place the dataset (`Mall_Customers.csv`) in the appropriate directory.
3. Execute the Python script or run the notebook.
4. Review WCSS values, cluster predictions, and final visualizations.

## Applications

Customer segmentation using clustering techniques is widely used in:
- Targeted marketing  
- Personalized recommendations  
- Customer lifetime value analysis  
- Optimizing promotional strategies  
- Behavioral analytics  

This project provides a foundational demonstration of how clustering can be used to support marketing and business decisions.
