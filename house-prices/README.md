# House Prices: Advanced Regression Techniques
Kaggle Competition

### Overview

Ask a home buyer to describe their dream house, and they probably won't begin with the height of the basement ceiling or the proximity to an east-west railroad. But this competition's dataset proves that much more influences price negotiations than the number of bedrooms or a white-picket fence.

With 79 explanatory variables describing (almost) every aspect of residential homes in Ames, Iowa, this competition challenges to predict the final price of each home.

Two similar datasets that include information on residential homes are provided in this competition. One dataset is titled `train.csv` and the other is titled `test.csv`.

The `train.csv` contains the details of residential homes in Ames, Iowa and importantly, reveals the actual price of each house.

The `test.csv` dataset contains similar information but does not disclose the sales price for each house. Using the patterns found in the train.csv data, the goal is to predict the sales price (the value of the SalePrice variable) for each Id in the test set. 

#### Acknowledgments
The [Ames Housing dataset](http://jse.amstat.org/v19n3/decock.pdf) was compiled by Dean De Cock for use in data science education. It's an incredible alternative for data scientists looking for a modernized and expanded version of the often cited Boston Housing dataset. 

#### Metric
Submissions are evaluated on Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price. (Taking logs means that errors in predicting expensive houses and cheap houses will affect the result equally.)

#### Submission File Format
The file should contain a header and have the following format:<br>
`Id,SalePrice`<br>
`1461,169000.1`<br>
`1462,187724.1233`<br>
`1463,175221`<br>
`etc.`

### Data Understanding

The graph below shows the distribution of actual house prices in the train dataset, `train.csv`.
![Distribution of House Prices](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/exploration1.png)

Notice that there are four examples whose GrLivArea values are greater than 4000. Those four examples are [recommended to be removed by the author](https://ww2.amstat.org/publications/jse/v19n3/decock.pdf).<br>
![GrLivArea vs SalePrice](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/exploration2.png)

### Data Modeling and Evaluation

The following five regression algorithms were used for data modeling - Ridge, Lasso, Elastic Net, Random Forest, and Gradient Boosting. RMSE and R-squared were used for model evaluation.

#### Ridge Regression
**RMSE**: 0.1078374048599644<br>
**R-Squared**: 0.8760133816113607<br>
![Ridge](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/ridge.png)

#### Lasso Regression
**RMSE**: 0.10476104575992143<br>
**R-Squared**: 0.8829865970559939<br>
![Lasso](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/lasso.png)

#### Elastic Net Regression
**RMSE**: 0.10462426253528934<br>
**R-Squared**: 0.883291959064217<br>
![Elastic Net](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/elasticnet.png)

#### Random Forest Regression
**RMSE**: 0.13171178092834698<br>
**R-Squared**: 0.815036854026564<br>
![Random Forest](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/randomforest.png)

#### Gradient Boosting Regression
**RMSE**: 0.11815725990431367<br>
**R-Squared**: 0.8511472777619353<br>
![Gradient Boosting](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/gradientboosting.png)

#### Evaluation Summary

The most ideal model is Elastic Net Regression with test set RMSE of 0.10462426253528934.<br><br>
![Evaluation](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/evaluation.png)

### Report

Prediction on examples in `test.csv` was performed using the Elastic Net Regression model. The graph below shows comparison between density distributions of real house prices in `train.csv` and predicted house prices of examples in `test.csv`.<br>
![Prediction](https://github.com/ynylgm/data-science-projects/blob/master/house-prices/images/prediction.png)


<br><br>
[nbviewer](https://nbviewer.jupyter.org/github/ynylgm/data-science-projects/blob/master/house-prices/house-prices.ipynb) for the notebook
<br><br>
Source: [Kaggle](https://www.kaggle.com/c/house-prices-advanced-regression-techniques)
