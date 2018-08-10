**IPL is full entertainment especially people who like cricket.It is total 40 overs entertainment.Any team can win based on its performance.It is very much hard to who will win a game as lots of factors are involved.What makes it more hard to predict is involvement of human factor.Because a player can win the match single handedly.


**Teams give their whole efforts to win the match.Certain times the team who win the toss can win the match because pitch varies with time.

**In our model we used following source files :

1.Trainmatches.csv
2.Testmatches.csv	
3.TrainDeliveries.csv
4.TestDeliveries.csv


**First below features engineering has been done for each season per team.It is then divided by no. of games played each team played for getting extra features per game per season.


1.powerplay_over_wickets = no. of wickets taken by each team during powerplay 
2.middle_over_wickets    = no. of wickets taken by each team during middle overs
3.death_over_wickets     = no. of wickets taken by each team during death overs
4.powerplay_runs         = Total runs scored by teams during powerplay
5.middle_over_runs       = Total runs scored by teams during middle overs
6.death_over_runs        = Total runs scored by teams during death overs
7.batting_strike_rate    = Batting strike rate by teams during tournament per season
8.bowling_economy_rate   = Bowling economy rate of teams during tournament per season



** For getting above features total_deliveries_stat is calculated from TrainDeliveries.csv and TestDeliveries.csv.

** It is then added with train matches  and test matchesfor getting all features.

** There are total 32 feature are there for predicting the value.

** For our prediction different  models are used like SVC,KNeighborsClassifier,RandomForestClassifier and xgboost.

** The best accuracy is given by xgboost with less over-fitting.
   *The accuracy of the xgb classifier is 0.70 out of 1 on training data
   *The accuracy of the xgb classifier is 0.54 out of 1 on test data

** Below hyperparameters are used in Xgboost as it is giving optimal performance

   learning_rate=0.01
   *num_boost_round = 2000
   *colsample_bytree=0.9
   *eta=0.3
   *eval_metric='mae'
   *max_depth=11
   *min_child_weight=7
   *subsample=1
** Below libraries as used.
   numpy
   pandas
   sklearn
