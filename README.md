In this repository we implement Hyper-Parameter Optimization (HPO) with [Hyperopt](https://archive.ics.uci.edu/dataset/14/breast+cancer). Hyperopt is an open-source python package that uses an algorithm called [Tree-based Parzen Estimators (TPE)][1] to select the best hyperparameters for a model. The implementation is applied on the [Breast Cancer Dataset](https://archive.ics.uci.edu/dataset/14/breast+cancer) and tested on five classification algorithms:

- K-Nearest Neighbor (KNN)
- Random Forest (RF)
- Support Vector Machine (SVM)
- Logistic Regression (LR)
- Naive Bayes (NB)

We do not focus on extensively preprocessing the data as we are primarily interested in the HPO process; therefore we do not follow complex steps before training the model. On some of the algorithms, the hyperparameter optimization process works better with scaling the data and thus the `MinMaxScaler` is fitted to the data before the process. The accuracy metric is measured before and after the HPO task to compare the performance of each algorithm.

[1]: https://proceedings.neurips.cc/paper_files/paper/2011/file/86e8f7ab32cfd12577bc2619bc635690-Paper.pdf