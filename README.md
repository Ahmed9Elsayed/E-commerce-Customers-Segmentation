# **E-commerce Customers Segmentation**

## Overview

This project aims to segment customers of an e-commerce platform into distinct groups based on their purchasing behavior and demographic data. By identifying different customer segments, businesses can tailor their marketing strategies and improve customer retention and satisfaction.

## Table of Contents

- [Overview](#overview)
- [Project Description](#project-description)
- [Dataset](#dataset)
- [Installation](#installation)
- [Usage](#usage)
- [Evaluation](#evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Contact Information](#contact-information)

## Project Description

In this project, I applied clustering algorithms to segment e-commerce customers based on their purchasing behavior and demographics. By using techniques such as **K-means**, **DBSCAN**, and **Hierarchical Clustering**, I was able to uncover meaningful patterns and distinct customer groups. Understanding these clusters can help improve customer retention, marketing campaigns, and personalized offers.

The goal is to group customers in a way that businesses can understand their behaviors and offer targeted services or products.

## Dataset

The dataset contains various customer features such as demographic information (e.g., age, gender, city) and purchasing behavior (e.g., transaction_status, Transaction date).

### Dataset Description:

Tdataset consisting of five interrelated tables, each containing crucial
information about customers, transactions, branches, and merchants. The tables are described
as follows:
1. Customers Table

	-  customer_id: Unique identifier for each customer.

	-  join_date: The date the customer joined.

	-  city_id: The ID representing the customer's city.

	-  gender_id: The ID representing the customer's gender.

1. Genders Table:

	-  gender_id: Unique identifier for each gender.

	-  gender_name: Name of the gender (e.g., male, female).

3. Cities Table:

	-  city_id: Unique identifier for each city.

	-  city_name: Name of the city.

4. Transactions Table:

	-  transaction_id: Unique identifier for each coupon transaction.

	-  customer_id: ID of the customer who performed the transaction.

	-  transaction_date: The date the coupon was claimed.

	-  transaction_status: Status of the coupon (e.g., claimed, burnt).

	-  coupon_name: The name of the coupon.

	-  burn_date: The date the coupon was burnt.

	-  branch_id: ID of the branch where the coupon was burnt.

1. Branches Table:

	-  branch_id: Unique identifier for each branch.

	-  merchant_id: ID of the merchant who owns the branch.

1. Merchants Table:

	-  merchant_id: Unique identifier for each merchant.

	-  merchant_name: Name of the merchant.


## Installation

To run this project, you need a Python environment with the following libraries installed:

- `pandas`
- `numpy`
- `scikit-learn`
- `matplotlib`
- `seaborn`
- `scipy`

You can install the dependencies using:


`pip install pandas numpy scikit-learn matplotlib seaborn scipy`

## Usage

1. **Load the Notebook:**
    
    - Open the notebook in Kaggle, Colab or your local Jupyter environment.

2. **Data Preprocessing and EDA:**
    
    - The notebook includes code for cleaning the data, handling missing values, and performing exploratory data analysis (EDA) to understand patterns in customer behavior.

3. **Feature Engineering:**

    - Feature Selection: selected only the most informative features

    - Feature Scaling: Scaled features to the same scale to avoid any disturbance that could show up with different scales

4. **Dimensionality Reduction:**
	- Visualized cumulative explained variance against the number of components after reduction to know how much variance(information) is captured of the whole data based on each number of reduced components using PCA

	- to reserve most of the information (85%) , I chose PCA components = 9

	- reducing Dimensionality using PCA has improved the Models performance and score

5. **Clustering Techniques:**

    - The following clustering techniques are implemented in this project:

        - **K-Means Clustering**

        - **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**

        - **Hierarchical Clustering**

    - Each algorithm is applied to the dataset to group customers into clusters based on the input features.


## Evaluation

### Evaluation Metrics:

- **Silhouette Score**: Evaluates how well each customer is clustered with its closest neighbors.
    
- **Davies-Bouldin Index**: Measures the average similarity ratio between each cluster and the cluster that is most similar to it.
    
- **K-Means**: The optimal number of clusters was determined using the **Elbow Method**, which gave the best Silhouette score with `n_clusters = 2`.
    
- **DBSCAN**: Parameters such as `eps` and `min_samples` were tuned based on the **K-distance plot**, and noise points were identified.
    
- **Hierarchical Clustering**: Dendrograms were used to visually determine the best number of clusters.
    

## Results


The results of the clustering techniques were compared, and the key findings are:

- **K-Means**: Created 2 distinct clusters that provided insights into customer coupon using habits.

- **DBSCAN**: Effectively identified noise in the data and formed dense clusters.

- **Hierarchical Clustering**: Showed clear relationships between clusters in a tree-like structure.

- All of these technique have reached to nearly the same 2 clusters

All of the clustering Techniques gave their highest results when clustering data into 2 clusters, which shows that natural grouping in our data is indeed 2 clusters 
### Silhouette score before Dimensionality Reduction
K-means =  0.2034

DBSCAN =  0.1741

Hierarchical Clustering =  0.2034
### Silhouette score after Dimensionality Reduction 
K-means = 0.2392 

DBSCAN = 0.2065 

Hierarchical Clustering = 0.2392 


## Conclusion

This project successfully segmented e-commerce customers into distinct groups based on their purchasing behavior and demographic information. The **K-Means / Hierarchical Clustering**  algorithms provided the best clusters, and this segmentation can help businesses better understand their customer base and optimize marketing strategies.

## Future Work

- Experiment with more advanced clustering algorithms, such as **Gaussian Mixture Models (GMM)** or **Self-Organizing Maps (SOM)**.


## Contact Information

If you have any questions or suggestions, feel free to contact me via Kaggle: [Kaggle Profile](https://www.kaggle.com/ahmed321abozeid) or at ahmedelsayedtaha467@gmail.com.