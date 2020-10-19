# encodings-for-categorical-data
Inspired by Jason Brownlee's tutorial [Ordinal and One-Hot Encodings for Categorical Data](https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/)

<br>Many machine learning models require all input and output variables to be numeric. This means that if your data contains categorical data, you must encode it to numbers before you can fit and evaluate a model. Encoding is a required pre-processing step when working with categorical data for machine learning algorithms.

There are three common approaches for converting ordinal and categorical variables to numerical values. They are:
* **Ordinal Encoding**: Each unique category value is assigned a integer value.
* **One-Hot Encoding**: The integer encoded variable is removed and one new binary variable is added for each unique integer value in the variable.
* **Dummy Variable Encoding**: Dummy variable encoding represents C categories with C-1 binary variables. The level with no dummy variable is known as the baseline.

In the notebook, demonstration for each of the three encoding methods was performed on the breast cancer dataset. The dataset classifies breast cancer patient data as either a recurrence or no recurrence of cancer. A logistic regression algorithm was used for the model.

In this particular case, the ordinal encoding model achieved the best classification accuracy of 75.79 percent, which is slightly better than the one-hot encoding and dummy variable encoding. One-hot encoding and dummy variable encoding resulted in the same accuracy score of 70.53 percent.

<br>Source: [Machine Learning Mastery](https://machinelearningmastery.com/one-hot-encoding-for-categorical-data/)
