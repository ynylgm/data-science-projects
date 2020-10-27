# Titanic: Machine Learning from Disaster
Kaggle Competition

### Overview

The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

This challenge requires to build a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

This competition provides access to two similar datasets that include passenger information like name, age, gender, socio-economic class, etc. One dataset is titled `train.csv` and the other is titled `test.csv`.

The `train.csv` will contain the details of a subset of the passengers on board (891 to be exact) and importantly, will reveal whether they survived or not, also known as the “ground truth”.

The `test.csv` dataset contains similar information but does not disclose the “ground truth” for each passenger. 

Using the patterns found in the `train.csv` data, predict whether the other 418 passengers on board (found in `test.csv`) survived.

#### Submission File Format:

The file should have 2 columns:

* PassengerId (sorted in any order)
* Survived (contains binary predictions: 1 for survived, 0 for deceased)

`PassengerId,Survived`<br>
`892,0`<br>
`893,1`<br>
`894,0`<br>
`Etc.`

### Data Understanding

Relationships between features Age, Sex, Pclass SibSp, Parch vs Survived are as shown on the graphs below.<br>
![Exploration1](https://github.com/ynylgm/data-science-projects/blob/master/titanic/images/exploration1.png)
![Exploration2](https://github.com/ynylgm/data-science-projects/blob/master/titanic/images/exploration2.png)

### Data Modeling and Evaluation

Machine learning algorithms that are used for data modeling are Random Forest, K-Nearest Neighbors, Decision Tree, Support Vector Classification. F1-score was used for evaluation.

![Evaluation](https://github.com/ynylgm/data-science-projects/blob/master/titanic/images/evaluation.png)

The ideal model is Random Forest Classifier with the highest F1-score of 0.852712.

### Report

Prediction on examples in `test.csv` was performed using the Random Forest Classifier.

**Survival Rate of Actual Data**: 0.3838383838383838<br>
**Survival Rate of Prediction**: 0.35406698564593303


<br><br>
[nbviewer](https://nbviewer.jupyter.org/github/ynylgm/data-science-projects/blob/master/titanic/titanic.ipynb) for the notebook

Source: [Kaggle](https://www.kaggle.com/c/titanic)
