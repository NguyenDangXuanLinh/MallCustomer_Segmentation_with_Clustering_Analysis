# Mall Customer Segmentation with Clustering Analysis
The project focuses on segmenting customers with unsupervised machine learning using K-means clustering.

## 1. Project Objectives

Through clustering analysis utilizing unsupervised machine learning techniques, specifically k-means clustering, we uncover distinct segments characterized by specific behaviors and attributes. This enables the formulation of targeted marketing strategies tailored to each segment's unique needs.

## 2. Analysis Techniques 
In the analysis process, I followed three critical steps to ensure robust and accurate clustering results:

1. _**Explorative Data Analysis (EDA)**_: visualizing data distributions, identifying outliers, and **uncovering initial patterns**  that later aided in verifying the performance of the k-means clustering results and **establishing criteria for effective segmentation**.
   
2. _**K-means Clustering Optimization**_: **optimization of hyperparameters** to achieve the best clustering results. To address the unsupervised nature of this learning method, I **used indirect metrics** to confirm the results:

   -  Utilized **Scree plot** (also known as an Elbow plot) to determine the **optimal number of clusters**.
   -  Calculate **Silhouette scores** and visualized it with heatmap to choose the **random state number.**
   -  **Plot Silhouette Score** to ensure consistency and confirm that there were **no wide fluctuations**, thereby validating the **stability of the clusters**."


3. _**Segmentation Results and Actionable Insights**_: employed the optimized hyperparameters to perform the clustering. Subsequently, I **visualized the 6 clusters** using a **3D plot**, assigned **meaningful names to each group**. To effectively **communicate my findings**, I used **box plots and bar plots** to highlight key insights and **recommendations among the top 4 customer segments**.

<br>

##  ✨ 3.1 Explorative Data Analysis (EDA)
### 3.1.1 Data distributions, understand and familiarize with the dataset
<img width="100%" align="middle" 
    src="image/numeric_dist.png">
    
<img width="50%" align="center" 
    src="image/sex_ratio.png">

<img width="100%" align="middle" 
    src="image/gender_range.png">

### 3.1.2 The potential relationships within our dataset that we expect to observe after applying the k-means clustering model

<img width="100%" align="middle" 
    src="image/spend_income_scatterplot.png">


<img width="100%" align="middle" 
    src="image/age_violinplot.png">

##  ✨ 3.3 Segmentation Results and Actionable Insights
### 3.3.1 Assigned Meaningful Names To Each Segment
<img width="100%" align="middle" 
    src="image/3D_plot.png">

### 3.3.2 Recommendations Among Top-4 Potential Customer Segments
<img width="100%" align="middle" 
    src="image/after_cluster_boxplot.png">
    
<img width="100%" align="middle" 
    src="image/groups_gender_barplot.png">


## ✨ 2.2 K-means Clustering Optimization

Before usng K-Means clustering, the parameter n_clusters, random_state needs to be found so that the model will perform the best. 

 - n_clusters -- Evaluate inertia values across different numbers and visualize it with the Elbow in the Scree Plot to find the proportition of variance.
 - random_state -- check with n-clusters using Silhoutte and heatmap
   
### 2.2.1 Find optimal number of clusters with scree plot
<img width="100%" align="middle" 
    src="image/clustering_screeplot.png">

### 2.2.2 Generate heatmap to visualize Silhouette Score against different the number of clusters and random states

So far, we confirmed that n_clusters=6 is the optimal value, but the random_state numbers have many numbers with the same Silhouette score. Therefore, we calculate Silhouette scores with different number of clusters and random state numbers then visualize it to choose paramaters that have Silhouette as close to 1 as possible since it is measured within range of (-1, 1). 

(The definition of Silhouette is explained in the plot)
<img width="100%" align="middle" 
    src="image/silhoutte_scatterplot.png">
    
### 2.2.3  Ensure the consistency and confirm that there were no wide fluctuation with the chosen hyperparameters

We will validate our choice by plotting Silhouette score against kmeans.labels_. The plot will be examined under these conditions:

- The presence of clusters are more or less of similar thickness and the size of the silhouette plots aren't in wide fluctuations.
- The average silhouette score is visualized by a red vertical line to confirm that Cluster scores should be higher than the average silhouette score.


<img width="100%" align="middle" 
    src="image/compare_silhouette_plot6.png">
#### ✨ We achieve these conditions with n_clusters=6 and random_state=10, n_init=30
<br>

#### For comparison purposes, we also generated the visualization with n_clusters set to 5 and 7.
<img width="100%" align="middle" 
    src="image/compare_silhouette_plot5.png">

<img width="100%" align="middle" 
    src="image/compare_silhouette_plot7.png">





    
