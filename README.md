Customer Segmentation using K-Means Clustering

#Project Overview

This project applies **unsupervised machine learning** to segment customers into meaningful groups based on their annual spending habits. Using the **Wholesale Customers Dataset** from the UCI Machine Learning Repository, 
the project identifies hidden customer patterns that can help businesses better understand purchasing behavior and improve decision-making.

The workflow includes:

* loading a real-world dataset,
* selecting important spending features,
* scaling the data,
* determining the best number of clusters using **silhouette score**,
* applying **K-Means clustering**,
* and visualizing the customer segments using **PCA**.


##Objectives

* Segment customers based on spending behavior
* Discover hidden patterns in customer purchasing data
* Find the optimal number of clusters using silhouette analysis
* Visualize the clusters in two dimensions using PCA
* Generate insights that can support marketing and business strategy

##Technologies Used

* Python
* Pandas
* Matplotlib
* Scikit-learn
* UCI ML Repository (`ucimlrepo`)

##Dataset

This project uses the **Wholesale Customers Dataset** from the **UCI Machine Learning Repository**.

### Features used for clustering:

* `Fresh`
* `Milk`
* `Grocery`
* `Frozen`
* `Detergents_Paper`
* `Delicassen`

These features represent annual spending amounts in different product categories.

##Project Workflow

### 1. Load Dataset

The dataset is loaded directly from the UCI Machine Learning Repository using `fetch_ucirepo`.

### 2. Feature Selection

Only the customer spending columns are selected for clustering:

* Fresh
* Milk
* Grocery
* Frozen
* Detergents_Paper
* Delicassen

### 3. Data Scaling

Since the features have different value ranges, **StandardScaler** is used to standardize the data before clustering.

### 4. Choosing the Best Number of Clusters

The project tests multiple values of `k` from **2 to 7** and evaluates each using the **silhouette score**.

### 5. K-Means Clustering

The best value of `k` is selected based on the highest silhouette score, and the final **K-Means** model is trained.

### 6. Cluster Summary

Average spending values for each cluster are calculated to understand the spending behavior of each customer segment.

### 7. PCA Visualization

**Principal Component Analysis (PCA)** reduces the scaled features to two dimensions so the clusters can be visualized on a 2D scatter plot.


## 📊 Result Visualization

### Customer Segments (PCA View)

<img width="2370" height="1765" alt="Customer segmentation" src="https://github.com/user-attachments/assets/dc632fc4-c958-40b5-8223-ceac8d12cf63" />


##Key Insights

* Customers were grouped into distinct segments based on their spending patterns.
* Most customers are concentrated in a dense central region, indicating similar purchasing behavior.
* A smaller group of customers appears farther from the main cluster, suggesting unusual or high-variance spending patterns.
* PCA helps simplify the high-dimensional customer data and makes cluster separation easier to understand visually.

##Machine Learning Techniques Used

* **K-Means Clustering**
* **StandardScaler**
* **Silhouette Score**
* **Principal Component Analysis (PCA)**

##How to Run the Project

### 1. Install required libraries

```bash
pip install ucimlrepo pandas matplotlib scikit-learn
```
### 2. Run the Python script or Jupyter Notebook

Make sure your script contains the clustering workflow and then run it.

##Future Improvements

* Add **Elbow Method** comparison along with silhouette score
* Use **Seaborn** or **Plotly** for more advanced visualizations
* Interpret each customer cluster in business terms
* Apply other clustering algorithms such as:

  * Hierarchical Clustering
  * DBSCAN
* Build an interactive dashboard for cluster exploration

##Contribution

Contributions are welcome. Feel free to fork this repository and improve the project.

##Support

If you found this project useful, consider giving it a **star** on GitHub.
