# Identification of NLOS-causing Material in UWB Localization Using Machine Learning Methods 📡🤖

## Research Result Table 📊

### Baseline MLP Binary Classification Experiment on Big Data

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 99.94%               |
| Precision | 99.96%               |
| Recall    | 99.94%               |
| F1-Score  | 0.9994               |

### Baseline MLP Material Classification Experiment

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 73.14%               |
| Precision | 73.05%               |
| Recall    | 73.14%               |
| F1-Score  | 0.7299               |

### Baseline MLP Multiclass Classification Experiment

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 86.69%               |
| Precision | 76.75%               |
| Recall    | 77.24%               |
| F1-Score  | 0.7690               |

### Baseline MLP Material Classification Experiment on Error Data

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 81.11%               |
| Precision | 81.29%               |
| Recall    | 81.27%               |
| F1-Score  | 0.8121               |

## Clustering

### Within-Cluster Sum of Squares (WCSS)
WCSS measures the variance of data points within each cluster. It quantifies how compact the clusters are. Smaller WCSS values indicate tighter clusters.

![Within-Cluster Sum of Squares (WCSS)](figures/WCSS.png?raw=true "Within-Cluster Sum of Squares (WCSS)")

### Silhouette Score
The silhouette score measures how similar each data point is to its own cluster compared to other clusters. A higher silhouette score indicates that the data points are well-separated into clusters.

![Silhouette Score](figures/silhouette_score.png?raw=true "Silhouette Score")

### Distortion Score Elbow for K-means Clustering
![Elbow Distortion](figures/elbow_plot.png?raw=true "Elbow Distortion")
