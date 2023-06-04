# README
This is the companion code repository for the paper **Modelling Point Mass Balance for the Glaciers of Central European Alps using Machine Learning Techniques** under review at The Cryosphere. The preprint can be found at: doi.org/10.5194/egusphere-2022-1076

This repository contains 3 directories. The files contained in each directory are listed below:

## main_code Directory
This directory contains the code and main results of the paper used for model inter-comparison. The files contained are:

1. complete_raw_code.ipynb: Main code that performs the regression using the models described in the paper. It includes feature importance analysis and variable dataset experiments.
2. training_predictions.csv: This csv file contains the predictions made by each model (as separate columns) for the training dataset. The true value is also represented as a column. The training metrics were derived from this dataset.
3. testing_predictions.csv: This csv file contains the predictions made by each model (as separate columns) for the testing dataset. The true value is also represented as a column. The testing metrics were derived from this dataset.

## hyp Directory
This directory contains the results of the hyperparameter tuning experiment. The details of the files in the directory are 

1. rf_grid.csv: This is the result of the hyperparameter tuning associated with the number of trees used in the random forest regressor.
2. gb_grid.csv: This is the result of the hyperparameter tuning associated with the number of trees, maximum depth and subsampling used in the gradient boosted regressor.
3. nn_grid.csv: This is the result of the hyperparameter tuning associated with the number of hidden layers and number of nodes in each hidden layer used in the neural network regressor.
4. svm_grid.csv This is the result of the hyperparameter tuning associated with the penalty parameter, kernel type and degree of polynomial (if kernel type is polynomial) used in the support vector machine regressor.

## feat_imp
This directory contains files associated with feature importance values for monthly meteorological variables for the models. The details of the files are as follows:

1. rf_perm_imp.csv: This file contains the permutation importance values associated with monthly meteorological variables for the random forest regressor.
2. gbr_perm_imp.csv: This file contains the permutation importance values associated with monthly meteorological variables for the gradient boosted regressor.
3. nn_perm_imp.csv: This file contains the permutation importance values associated with monthly meteorological variables for the neural network regressor.
4. svm_perm_imp.csv: This file contains the permutation importance values associated with monthly meteorological variables for the upport vector machine regressor.
5. lr_perm_imp.csv: This file contains the permutation importance values associated with monthly meteorological variables for the linear regressor.

## Additional Files
In addition to the files within the direcories, one zip file with the trained models is available at trained_models.zip.

Additionally, the code for additional runs including the changing of normalization technique can be found at: https://colab.research.google.com/drive/1dCJfrNoGPv9s1A2eD0Y2BGHILZzrzc2i?usp=sharing
