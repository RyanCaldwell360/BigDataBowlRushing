# BigDataBowlRushing
Retroactively going back and replicating top submission ideas/solutions. Mainly as practice prep for future competitions.

## Data Prep
Because of data size I wasn't able to include the train.csv file in the /data folder. So you would just need to download it from kaggle and store there.
https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/data

So far I'm really only considering the 11 defensive players relative to the rusher. This includes their distance, speed, acceleration and direction from the rusher. I also used KNN to find the 10 most similar rusher/plays to extract Yards distribution features (min, max, mean and standard deviation of Yards). I also have the static rusher info of X, Y, S, A, Dir.

This sort of setup is heavily influenced by the following: https://www.kaggle.com/competitions/nfl-big-data-bowl-2020/discussion/119400. I need to spend more time understanding their offense X defense X features setup, but I believe my rusher X defense x features is almost there.

## Model(s)

#### CNN Yards Prediction
1. convolusions over defense vs rusher data (rusher x defense x feature; (batch_size,1,11,4))
1. dense over rusher features
1. dense 1 output head for regression prediction
1. dense X output head for capped yards CRPS prediction; need to figure out what to cap predictions between

#### CNN Formation Prediction
It seems that it might be helpful to have a block of offense vs defense features to be used by CNN to predict formation types. Maybe then have 2 output heads (1 for offensive formation and 1 for defensive formation) where both are multiclass predictions. This might be an interesting way to extract formation embeddings that encode how players are aligned through space.