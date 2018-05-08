# Word2Vec-for-sequential-categorical-data

The reason I create this repository is that I found some interesting method to improve the behavior of using xgboost or lightgbm on encoded label sequential data. This repository is based on the Kaggle challenge TalkingData AdTracking Fraud Detection Challenge, where I also create a kernel for this idea.

## Some result.

After using W2V to create a 'word embedding' to the categorical data, in this case it is app, device, os and channel (The size of word embedding is 3 in this case due to the large size of dataset.), the auc score have increased comparing with the label encoded categorical data. The reason of this increasing is that after using word embedding ideas, we actually dig out the relationship between different categories, for example, what is the relationship between app 9 and app 10? This relationship is independent with the users, which means it isn't influenced by specific behavior of users. 

With the increasing of 'word embedding' size, the behavior will become better and better but this increasing is with the cost of time.

Also, now we can use NN as another method to train the data where we get some consecutive numbers in each dimensions.

Details can be found in my kernel.

https://www.kaggle.com/jingqliu/xgboost-nn-on-small-sample-with-word2vec

https://www.kaggle.com/jingqliu/nn-with-word2vec-large-embeddings
