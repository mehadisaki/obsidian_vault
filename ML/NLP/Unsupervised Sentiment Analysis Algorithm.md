<tag> Extract sentiment from any text</tag>


There are two main approaches you could take, to teach an algorithm to distinguish between positive and negative emotions in writing — a supervised, and an unsupervised one.

1. The first one would inquire from you to collect labeled data, and teach an algorithm (e.g. [LSTM](https://skymind.ai/wiki/lstm) network) in a supervised manner how each word in a sequence (actually all words appearing one after another, if we talk about [RNNs](https://skymind.ai/wiki/lstm)) corresponds to the outcome of overall sentence being negative or positive.

2. The latter approach would be an unsupervised one, and this one is an object of interest in this article. The main idea behind unsupervised learning is that you don’t give any previous assumptions and definitions to the model about the outcome of variables you feed into it — you simply insert the data (of course preprocessed before), and want the model to learn the structure of the data itself.

3. One of the most important ideas in recent breakthroughs both in NLP and computer vision was efficient usage of transfer learning. In the field of NLP most of transfer learning happens in a way, that some model (let it be MLP in case of Word2Vec, or transformer like [BERT](https://medium.com/dissecting-bert/dissecting-bert-part-1-d3c3d495cdb3)) is at first trained in unsupervised manner (actually fake supervised) on the data, and then fine tuned on specific task, or just used in another model to produce better quality features. Usually, it is given a fake supervised task, such as predicting word based on words that surround it, or predict surrounding words based on a given word (see: [word2vec](http://mccormickml.com/2016/04/19/word2vec-tutorial-the-skip-gram-model/)), or predict next word/sentence based on previous words/sentences ([transformer models](http://jalammar.github.io/illustrated-transformer/)).


