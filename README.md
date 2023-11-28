# Identification of NLOS-causing Material in UWB Localization Using Machine Learning Methods 📡🤖
## 🚀 Welcome to the world of Ultra-Wideband (UWB) technology! 🌐

UWB has taken the tech world by storm with its pinpoint location tracking, snappy short-range communication, and cool applications in IoT, smart homes, and the automotive realm. 📡🏠🚗

But wait, there's a twist! 🔄

Enter the Non-Line-of-Sight (NLOS) conundrum 🌫️. Sometimes, UWB signals go all detective mode, bouncing off obstacles and reflective surfaces, causing delays and messing up distance measurements. 😬

Imagine your GPS telling you that you're casually swimming in the nearby lake when you're just sipping coffee at a cafe nearby. NLOS can be that sneaky. 🏊‍♂️🍵

That's where this repo swoops in with capes and machine learning magic! ✨

While using machine learning to tackle signal hiccups isn't new, it's all the rage right now. 🧙‍♂️✨

But, here's the scoop: Most research focuses on sorting things into either "Line-of-Sight" or "Non-Line-of-Sight." We're here to make things more interesting and fine-tuned! 🤓

This project aims to bring some order to the NLOS chaos. 🧐

The idea? Different NLOS-causing materials might have unique quirks, or one can group them into categories like "soft-NLOS" or "hard-NLOS." 🤖📊

So, if you're ready to dive into the world of UWB, machine learning, and a sprinkle of detective work, welcome aboard! 🕵️‍♀️🚀

## Repository Structure

- 📦 **archieve**
   - This folder hosts everything that was important but is no longer in the spotlight.

- 📊 **baseline_classification**
   - Welcome to the lab! Here, we conduct all our baseline experiments, the foundational tests of our project.

- 📈 **data_analysis**
   - Think of this folder as our data playground. Here, we dive deep into numbers, charts, and graphs to uncover hidden insights and patterns.

- 🖼️ **figures**
   - In this folder, we treasure our visual gems. These are the figures and visuals that bring our data to life. Safety first, so they have their own special place.

- 🚀 **final_experiments**
   - This is where the magic happens! We keep the most valuable experiments here, the ones that truly emphasize our theories and findings. It's where we showcase the crown jewels of our research.


## Research Result Table 📊

### Baseline MLP Binary Classification Experiment on Big Identification Data

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 99.94%               |
| Precision | 99.96%               |
| Recall    | 99.94%               |
| F1-Score  | 0.9994               |

### Baseline MLP Material Classification Experiment on Big Identification Data

| Metric    | Value                |
|-----------|----------------------|
| Accuracy  | 73.14%               |
| Precision | 73.05%               |
| Recall    | 73.14%               |
| F1-Score  | 0.7299               |

### Baseline MLP Multiclass Classification Experiment on Big Identification Data

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

## Clustering on Error Data

### Within-Cluster Sum of Squares (WCSS)
WCSS measures the variance of data points within each cluster. It quantifies how compact the clusters are. Smaller WCSS values indicate tighter clusters.

![Within-Cluster Sum of Squares (WCSS)](figures/WCSS.png?raw=true "Within-Cluster Sum of Squares (WCSS)")

### Silhouette Score
The silhouette score measures how similar each data point is to its own cluster compared to other clusters. A higher silhouette score indicates that the data points are well-separated into clusters.

![Silhouette Score](figures/silouette_score.png?raw=true "Silhouette Score")

### Distortion Score Elbow for K-means Clustering
![Elbow Distortion](figures/elbow_plot.png?raw=true "Elbow Distortion")

## SVM
| kernel   |   accuracy |   precision |   recall |       f1 |   train_time_per_sample |   test_time_per_sample |
|:---------|-----------:|------------:|---------:|---------:|------------------------:|-----------------------:|
| rbf      |   0.806898 |    0.804855 | 0.806395 | 0.806395 |             0.000968527 |            0.00228607  |
| linear   |   0.856783 |    0.855553 | 0.856039 | 0.856039 |             0.00212661  |            0.000734085 |
| poly     |   0.708303 |    0.736    | 0.707387 | 0.707387 |             0.00161534  |            0.00087245  |
| sigmoid  |   0.527966 |    0.551219 | 0.52752  | 0.52752  |             0.00123145  |            0.00107637  |

## MLP
| hidden_layer_sizes       |   accuracy |   precision |   recall |       f1 |   train_time_per_sample |   test_time_per_sample |
|:-------------------------|-----------:|------------:|---------:|---------:|------------------------:|-----------------------:|
| (50,)                    |   0.98186  |    0.982025 | 0.982028 | 0.982028 |             0.00139544  |            5.787e-07   |
| (50, 50)                 |   0.991154 |    0.99135  | 0.991123 | 0.991123 |             0.00128966  |            1.33319e-06 |
| (50, 50, 50)             |   0.988019 |    0.988097 | 0.98822  | 0.98822  |             0.000961179 |            1.56593e-06 |
| (50, 50, 50, 50)         |   0.98046  |    0.981017 | 0.980441 | 0.980441 |             0.000818557 |            2.89977e-06 |
| (50, 50, 50, 50, 50)     |   0.980404 |    0.980523 | 0.980583 | 0.980583 |             0.000880122 |            3.19842e-06 |
| (50, 50, 50, 50, 50, 50) |   0.983875 |    0.98393  | 0.984097 | 0.984097 |             0.00145     |            4.61586e-06 |

## RF
|   number_of_trees |   accuracy |   precision |   recall |       f1 |   train_time_per_sample |   test_time_per_sample |
|------------------:|-----------:|------------:|---------:|---------:|------------------------:|-----------------------:|
|                 5 |   0.8719   |    0.873856 | 0.87239  | 0.87239  |             1.28354e-05 |            1.12619e-06 |
|                10 |   0.901237 |    0.902022 | 0.90161  | 0.90161  |             2.03947e-05 |            1.96707e-06 |
|                20 |   0.904597 |    0.905448 | 0.904936 | 0.904936 |             4.03076e-05 |            3.68428e-06 |
|                30 |   0.906892 |    0.907208 | 0.907242 | 0.907242 |             6.0645e-05  |            5.43059e-06 |
|                50 |   0.910475 |    0.910688 | 0.910839 | 0.910839 |             0.000100613 |            8.82269e-06 |
|               100 |   0.913779 |    0.914085 | 0.91412  | 0.91412  |             0.000201685 |            1.75537e-05 |
|               200 |   0.913779 |    0.914384 | 0.914084 | 0.914084 |             0.000403243 |            3.5128e-05  |
|               500 |   0.913779 |    0.91414  | 0.914113 | 0.914113 |             0.000999109 |            8.805e-05   |