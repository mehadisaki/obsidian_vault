
In contrast to stemming, lemmatization looks beyond word reduction, and considers a language’s full vocabulary to apply a morphological analysis to words. The lemma of ‘was’ is ‘be’ and the lemma of ‘mice’ is ‘mouse’. Further, the lemma of ‘meeting’ might be ‘meet’ or ‘meeting’ depending on its use in a sentence.

NLTK’s lemmatizer requires a positional argument, if don’t give the positional tag, it’ll take the word as a noun and not performs the lemmatization. You can see below in the snippet, after giving the proper positional tag the lemmatization performs better.