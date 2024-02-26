![[Pasted image 20231107224742.png]]



## Embedding based models

Text embeddings are a form of word representation in NLP in which synonymically similar words are represented using similar vectors which when represented in an n-dimensional space will be close to each other.

![word vectors](https://i0.wp.com/neptune.ai/wp-content/uploads/2022/10/word-vectors.png?resize=580%2C336&ssl=1)

Embedding based python packages use this form of text representation to predict text sentiments. This leads to better text representation in NLP and yields better model performance.

One of such packages is Flair.    

### **Flair** 

[Flair](https://github.com/flairNLP/flair) is a simple to use framework for state of the art NLP. 

It provided various functionalities such as:

- pre-trained sentiment analysis models, 
- text embeddings, 
- NER, 
- and more.

Let’s see how to very easily and efficiently do sentiment analysis using flair.

Flair pretrained sentiment analysis model is trained on IMDB dataset. To load and make prediction using it simply do:

``` python
from flair.models import TextClassifier
from flair.data import Sentence

classifier = TextClassifier.load('en-sentiment')
sentence = Sentence('The food was great!')
classifier.predict(sentence)
```

# print sentence with predicted labels
print('Sentence above is: ', sentence.labels)

[POSITIVE (0.9961)

If you like to have a custom sentiment analyzer for your domain, it is possible to train a classifier using flair using your dataset.

The drawback of using a flair pre-trained model for sentiment analysis is that it is trained on IMDB data and this model might not generalize well on data from other domains like twitter.

