
Topic modeling algorithms commonly used in machine learning models with Python include:

1. **Latent Dirichlet Allocation (LDA):** LDA is a probabilistic model that assumes documents are mixtures of topics and words are mixtures of topics. It is widely used for topic modeling.

   - Python Library: `gensim`, `scikit-learn`

2. **Latent Semantic Analysis (LSA):** LSA is a dimensionality reduction technique that is often used for topic modeling. It uses singular value decomposition (SVD) to find patterns in term-document matrices.

   - Python Library: `scikit-learn`

3. **Non-Negative Matrix Factorization (NMF):** NMF factorizes a term-document matrix into two lower-dimensional matrices. It is useful for finding topics in text data.

   - Python Library: `scikit-learn`

4. **Hierarchical Dirichlet Process (HDP):** HDP is an extension of LDA that allows for a potentially infinite number of topics. It's useful when the number of topics is unknown.

   - Python Library: `gensim`

5. **Correlated Topic Model (CTM):** CTM is an extension of LDA that models correlations between topics. It's useful when topics are expected to be related.

   - Python Library: `gensim`

6. **Online LDA:** Online LDA is a variation of LDA that can be trained incrementally on streaming data. It's useful for handling large datasets.

   - Python Library: `gensim`

7. **Word Embedding-based Approaches:** Algorithms like Word2Vec and Doc2Vec can be used for topic modeling by capturing semantic relationships between words and documents.

   - Python Libraries: `gensim`, `spaCy`

8. **BERTopic:** BERTopic is an algorithm that uses transformers like BERT to discover topics in documents. It's known for its effectiveness in capturing context.

   - Python Library: `bertopic`

9. **BigARTM:** BigARTM (Big Additive Regularization Topic Model) is a scalable topic modeling library that supports various types of regularization.

   - Python Library: `bigartm`

10. **FastText:** While primarily designed for text classification and word embeddings, FastText can also be used for topic modeling by clustering word vectors.

    - Python Library: `fasttext`

These algorithms are used to discover underlying topics within a corpus of text data and are widely applied in natural language processing (NLP) and text mining tasks. The choice of algorithm depends on factors such as the size of the dataset, the desired number of topics, and the specific characteristics of the text data.




1. LiLT model for Information extraction from Image and PDF documents
2. 
