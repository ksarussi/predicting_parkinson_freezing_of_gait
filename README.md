# Detecting Parkinson's Symptoms
Kaggle competition predicting Parkinson's Freezing of Gait (FOG) for final project in MSCA 31013

Evy Park, Katy Barone, Kelley
Sarussi & Zander Meitus - Spring 2023

https://www.kaggle.com/competitions/tlvmc-parkinsons-freezing-gait-prediction/overview

Many with Parkinson's Disease experience “Freezing of Gait” (FOG), a symptom
characterized by trouble stepping. FOG “impairs balance, increases falls, and
reduces the quality of life” and is currently not well understood by the medical
community.

This project aims to predict FOG based on data from motion sensors worn by
patients with Parkinson's. The FOG symptom types include start hesitation, turning, and walking.

## Data

The data is stored in a Google Cloud bucket due to size constraints (data is approximately 70gb in size).

1. Labeled Data (defog and tdcsfog): Sensor data from patients undergoing medical
testing; designed to induce FOG
2. Unlabeled Data: One week of unlabeled, continuous daily living sensor recordings
3. Metadata: Provides labels for data series on subjects, FOG,  and task

## Files

1. /utils 
    - utils.py: helper functions for cleaning data
2. eda.ipynb
    - exploratory data analysis
3. combine_datasets.ipynb
    - feed and combine defog and tdcsfog files (labeled data) into a compiled training dataset
4. combine_defog.ipynb
    - feed and combine defog files into fog training data
5. combine_unlabeled_daily.ipynb
    - combine unlabeled data into one complete dataset
6. cluster_lag_feature_creation.ipynb
    - add additional features to unlabeled data 
    - run k-means clustering model on unlabeled data
7. load_fog_with_subjects.ipynb
    - load fog data with metadata
8. logreg.ipynb
    - logistic regression model and feature engineering
9. make_tasks.ipynb
    - join tasks data with fog, transform target variable
10. tree_models.ipynb
    - decision tree and random forest models
