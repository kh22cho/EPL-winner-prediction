# EPL-winner-prediction
* This is project result of first semester of 24 years that class name is AI in Bioinformatics.
* Purpose is to predict season winner using previous season data.
* I took a lot of reference from this [github](https://github.com/ClassifiedEgg/Predicting-EPL-Season-using-Machine-Learning?tab=readme-ov-file). Thank you.

## Model
* Project model is Random Forest but you can apply another method.

## Data
* You can download season data in [this](https://www.football-data.co.uk/) and [this](https://fixturedownload.com/).
* Also this is [TransferMarket](https://www.transfermarkt.com/).

## Feature
* Define two major terms that __Strength__ and __Power__.
* Strength is the value defined by how strong the home team is at home and the away team.
  * Home Attack Strength = Home Average Scores * Away Average Conceded.
  * Away Attack Strength = Away Average Scores * Home Average Conceded.
* Power is the  value defined by 5-years __Relative Record__.
  * Calculate ratio like (Win + Draw / total matches).
  * If it's the first match each teams met than using Imputer to fill median value.

## Intense match or Not
* The more match is intense, the more difficult to predict.
* The matches model prediction failed are contain more intense matches.
* In this step, I defined Intense match is match in which the absolute value of the difference between the total goals is 2 or less.

## Discussion
* Therefore, I decided that if the hyperparameter is adjusted too much, overfitting may occur.
* Football games are too difficult to predict, so I decided that it was more important to handle the data well.
* Also I think it would be helpful to learn the model in the direction of further reducing intense matches among the match that failed in prediction.
