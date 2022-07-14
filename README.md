# BigDataBowlRushing
Retroactively going back and replicating top submission ideas/solutions. Mainly as practice prep for future competitions.

## Data Prep
Because of data size I wasn't able to include the train.csv file in the /data folder. So you would just need to download it from kaggle and store there.
https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/data

So far I'm really only considering the 11 defensive players relative to the rusher. This includes their distance, speed, acceleration and direction from the rusher. I also used KNN to find the 10 most similar rusher/plays to extract Yards distribution features (min, max, mean and standard deviation of Yards). I also have the static rusher info of X, Y, S, A, Dir.

This sort of setup is heavily influenced by the following: https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/discussion/119400. I need to spend more time understanding their offense X defense X features setup, but I believe my rusher X defense x features is almost there.
