# House Prices: Advanced Regression Techniques (Kaggle)

This repo contains the jupyternotebook, codes, and results associated with my submission to the kaggle competition located at:
https://www.kaggle.com/c/house-prices-advanced-regression-techniques/leaderboard#score

The notebook leverages numerous functions related to model comparison and grid search across multiple different sci-kit learn & keras-based models. These helper functions are contained in a the python package at:
https://github.com/jlnerd/JLpy_utils_package

Overall, the notebook demonstrates how to achieve an root mean square log error (RMSLE) of ~0.128 by searching through various feature engineering techinques (with and without one-hot encoding, with and without log-transformation on the label of interest), and by running grid search CV on numerous models. The models evaluated are:

1. Linear
2. SVM
3. KNN
4. Decision Tree
5. Random Forest
6. Grad Boost Forest
7. Dense Neural Network

Aside from the RMSLE score itself, the notebook highlights some interesting insights on how these various types of models behave better or worse depending on the structure of the features they are being trained on. These are particularly interesting for the case of the neural networks, where we see the dense neural network is the works performing model without log transforming the labels of interest, while it is one of the best models when we apply log transformation to the labels. All in all though, the grad boosted forest prooved to be the best model. 

In terms of relative importance of this ~0.128 score on the Kaggle test set, the 5th place score on Kaggle (as of Aug 6th, 2019) is ~0.10369, thus the submission outline here is ~1.234 times worse than 5th place.

