# Natural Language Processing with Disaster Tweets
Kaggle Competition

### Overview

#### Competition Description
Twitter has become an important communication channel in times of emergency. The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

But, it’s not always clear whether a person’s words are actually announcing a disaster.

In this competition, build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t using access to a dataset of 10,000 tweets that were hand classified.

Disclaimer: The dataset for this competition contains text that may be considered profane, vulgar, or offensive.

#### Acknowledgments
This dataset was created by the company figure-eight and originally shared on their [‘Data For Everyone’ website here](https://www.figure-eight.com/data-for-everyone/).

#### Evaluation
Submissions are evaluated using F1 between the predicted and expected answers.

F1 is calculated as follows:

<p align="center">
<img align="middle" src="https://latex.codecogs.com/png.latex?\bg_white&space;F1=2\times&space;\frac&space;{precision\times&space;recall}&space;{precision&plus;recall}" title="F1=2\times \frac {precision\times recall} {precision+recall}" />
</p>

where:

<p align="center">
<img src="https://latex.codecogs.com/png.latex?\bg_white&space;precision=&space;\frac&space;{TP}&space;{TP&plus;FP}" title="precision= \frac {TP} {TP+FP}" /><br>
<img src="https://latex.codecogs.com/png.latex?\bg_white&space;recall=&space;\frac&space;{TP}&space;{TP&plus;FN}" title="recall= \frac {TP} {TP+FN}" />
</p>

and:

> True Positive [TP] = your prediction is 1, and the ground truth is also 1 - you predicted a *positive* and that's *true*!<br>
False Positive [FP] = your prediction is 1, and the ground truth is 0 - you predicted a *positive*, and that's *false*.<br>
False Negative [FN] = your prediction is 0, and the ground truth is 1 - you predicted a *negative*, and that's *false*.<br>

#### Submission File
For each ID in the test set, `1` if the tweet is describing a real disaster, and `0` otherwise. The file should contain a header and have the following format:

`id,target`<br>
`0,0`<br>
`2,0`<br>
`3,1`<br>
`9,0`<br>
`11,0`<br>

### Data Understanding

The number of tweets, lengths of tweets, number of words in tweets by target values (`0` - Not Disaster, `1` - Disaster) are visualized as below.

<p align="center">
<img src="https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/target.png">
<img src="https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/length.png">
<img src="https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/words.png">
</p>

Some of the most tweeted keywords and locations are shown on the graphs below.

<p align="center">
<img src="https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/keyword.png">
<img src="https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/location.png">
</p>

### WordClouds
Below is the word clouds of Not-Disaster Tweets and Disaster Tweets created after the data cleaning process.

![wordclouds](https://github.com/ynylgm/data-science-projects/blob/master/disaster-tweets/images/wordcloud.png)

### Data Modeling and Evaluation

TF-IDF Vectorizer and Ridge Classifier (classifier using Ridge regression) were used for data modeling and as per instructions, F1 score was used for evaluation. The cross-validation scores are as follows:<br>
[0.59885932 0.48958333 0.56503015 0.55747126 **0.67810458**]<br>
It looks like the predictions will score roughly 0.68 on the leaderboard.

<br><br>
[nbviewer](https://nbviewer.jupyter.org/github/ynylgm/data-science-projects/blob/master/disaster-tweets/disaster-tweets.ipynb) for the notebook

Source: [Kaggle](https://www.kaggle.com/c/nlp-getting-started/)
