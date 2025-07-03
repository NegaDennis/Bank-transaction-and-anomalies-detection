# Bank-transaction-and-anomalies-detection


Full Analyis files can be found in the 'code' folder of this repository.

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
Some interesting insights were observed from the EDA stage. Some of the highlights include:
- Monday is the most busy day in term of transactions traffic for the bank:
  ![1](https://github.com/user-attachments/assets/97866956-11e8-4d37-adf8-41ffd33e27b6)
  
- Most transactions take between 50 seconds and 150 seconds:
  ![2](https://github.com/user-attachments/assets/7c4e21d8-962f-47d0-9d44-47d9c5e909c5)
  
ML modelling on the dataset was a success. The model was successful at producing a map with 3 clusters. The clusters could be described as below:
- Cluster 0: it includes transactions that are low in dollar amount and takes less time to transact.
- Cluster 1: Despite higher transaction duration, the members of this cluster deals mostly in small dollar amounts.
- Cluster 2: Members tend to take longer time to transact and deals in higher dollar amounts.
![3](https://github.com/user-attachments/assets/c7bb0412-a98e-4921-87c1-5fcb5d8af7f6)

After calculating distance and threshold, the model detected 126 anomalies in the dataset with abnormally long durations and high transaction amounts.
![4](https://github.com/user-attachments/assets/d12ae3f3-7ae0-4eb1-af12-d7de654f69bf)


## Conclusions and limitations
The model satisfied the purpose of the project, making interpretable detections of anomalies within the dataset. The model also have potential to scale with number entries and number of features to include.

There are rooms for improvement for future model development attempt. Here are a few ways to build up on this project's outcomes:
- Try different types of model to detect anomalies. This includes DBSCAN, Hierarchical Clustering, Spectral Clustering, and more.
- Adding more features to the model. (This will, however, increase model complexity and trade off interpretability)
- Perform further data manipulation to engineer new features.
- Fit the model on more data.

For future projects, one of more options will be employed to seek better performance.
