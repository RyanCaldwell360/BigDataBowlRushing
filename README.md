# BigDataBowlRushing
Retroactively going back and replicating top submission ideas/solutions. Mainly as practice prep for future competitions.

## Data Prep
Because of data size I wasn't able to include the train.csv file in the /data folder. So you would just need to download it from kaggle and store there.
https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/data

So far I'm really only considering the 10 offensive players (exluding the RB) and 11 defensive players relative to each other and the RB. I played around with adding additional features than here: https://www.kaggle.com/code/jccampos/nfl-2020-winner-solution-the-zoo, but didn't have any success. So the blocks of features are represented by the 10x11x10 (OFFxDEFx10 features).

I'd like to introduce RB specific features that I could concat in the last dense layers prior to the output layer. It might also be helpful to include game situation type features as well. This might end up being a decent proxy for how offenses and defenses align and what type of play call is executed.