# Bank-transaction-and-anomalies-detection


It's a work in progress!!! Almost done. Just need to furnish this README with images and some EDA highlight next. Read v3 code file in 'code' folder for latest version.

## Data understanding


The dataset is a direct copy of the Bank Transaction Dataset for Fraud Detection from Kaggle. The dataset was last updated on 04/11/2024.


This dataset provides a detailed look into transactional behavior and financial activity patterns, ideal for exploring fraud detection and anomaly identification. It contains 2,512 samples of transaction data, covering various transaction attributes, customer demographics, and usage patterns. Each entry offers comprehensive insights into transaction behavior, enabling analysis for financial security and fraud detection applications.

The dataset was synthesized based on realistic bank transaction patterns from publicly available sources, including research studies, industry reports, fraud detection surveys and other relevant studies.


The dataset is made up of individual transactions made from 2023-01-03 to 2024-01-02,


Link: https://www.kaggle.com/datasets/valakhorasani/bank-transaction-dataset-for-fraud-detection


## Motivation

This is a practice of EDA and machine learning application on banking data.

At the end of the project, the goals include:
1. Performed well-coded EDA with valueable insights.
2. Developed a clustering model that properly segment transactions and accounts.
3. Codes are well-documented and pythonic.


## Model development process

A clustering model was developed using KNN method. The model utilized the sklearn library.

The variables included in the model are TransactionDurations and TransactionAmount. Both was directed through a standard scaler from the sklearn library before model fitting. By observing interia/k-number trade-off and the elbow method, k=3 was found to be the optimal number of neighbors and was used for the model.


## Result
The model was successful at producing a map with 3 clusters. The clusters could be described as below:
- Cluster 0: it includes transactions that are low in dollar amount and takes less time to transact.
- Cluster 1: Despite higher transaction duration, the members of this cluster deals mostly in small dollar amounts.
- Cluster 2: Members tend to take longer time to transact and deals in higher dollar amounts.

After calculating distance and threshold, the model detected 126 anomalies in the dataset with abnormally long durations and high transaction amounts.


## Conclusions and limitations
The model satisfied the purpose of the project, making interpretable detections of anomalies within the dataset.

There are rooms for improvement for future model development attempt. Here are a few ways to build up on this project's outcomes:
- Try different types of model to detect anomalies. This includes DBSCAN, Hierarchical Clustering, Spectral Clustering, and more.
- Adding more features to the model. (This will, however, increase model complexity and trade off interpretability)
- Perform further data manipulation to engineer new features.
- Fit the model on more data.

For future projects, one of more options will be employed to seek better performance.
