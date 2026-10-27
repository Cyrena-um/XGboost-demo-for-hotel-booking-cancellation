This repository is an XGboost demonstration for prediction and comprehension of hotel booking cancellation. The data is real hotel data collected and published by Antonio, de Almeida and Nunes in Protugal. Two datasets, one describing resort hotels and another about city hotels, were shared for research and educational purposes. The time span of the data ranges from July 1, 2015 and Aug 31, 2017, with 40,060 samples from resort hotels and 79,330 samples from city hotels. It contains 27 valid variables aiming to predict the cancellation of the reservation. The distribution of the outcome variable is slightly imbalanced (74745 arrivals vs 44153 cancellations)[^1].



In this repo, XGboost is utilized to predict the booking cancellation. The jupyter notebook begins with preprocessing and cleaning the raw data. Descriptive statistics and relevant plots are then displayed to understand the overview of the data.  As the datasets involve date, train and test datasets are split according to the date to avoid data leakage. Similar precautions should be taken on subsequent cross validation.  After cross validation is conducted on train dataset to configure the hyperparameters, the model is refined with permutation importance scores. With a second model with selected features only, cross validation has to be repeated to extract the new hyperparameters. In order to maximize the performance, default threshold is dismissed and a new threshold is determined by F1-score. At last, SHAP analysis is performed on the resulting model to explore the characteristics of cancellations.



[^1]: Antonio, N., de Almeida, A., \& Nunes, L. (2019). Hotel booking demand datasets. Data in brief, 22, 41-49.

