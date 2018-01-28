# Non-Negative-matrix-factorization
Non-Negative matrix factorization- An intuitive dimension reduction method


NMF is Non-Negative matrix factorization. This is also a dimension reduction method but more intuitive than PCA. “Unlike PCA, NMF does learn the parts of things. Its components correspond to topics (in the case of documents) or to parts of images when trained on images. Topic Models are very useful for the purpose for document clustering, organizing large blocks of textual data, information retrieval from unstructured text and feature selection. 

Both PCA and NMF are matrix factorizations. For PCA, a singular value decomposition (SVD) factors the correlation matrix (R) into the product of factor loadings (F): R = FF’. NMF, on the other hand, decomposes the data matrix (V) into the product of W and H. The term “nonnegative” indicates that all the cells in all three matrices must be zero or greater. 



Speaking loosely, one might say that PCA returns latent dimensions and NMF generates latent features or categories.  

LDA is a probabilistic model capable of expressing uncertainty about the placement of topics across texts and the assignment of words to topics, NMF is a deterministic algorithm which arrives at a single representation of the corpus. Like LDA, NMF arrives at its representation of a corpus in terms of something resembling “latent topics”.
