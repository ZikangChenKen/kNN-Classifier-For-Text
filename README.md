# kNN-Classifier-For-Text
A kNN classiﬁer to classify text documents. The implementation will be in Python, on top of Spark.

Wrote Spark code that builds a dictionary that includes the 20,000 most frequent words in the training corpus.

Wrote Spark code that converts each of those 19,997 count vectors to TF-IDF vectors.

Built a kNN classiﬁer, embodied by the Python function predictLabel. This function will take as input a text string and a number k, and then output the name of one of the 20 newsgroups. This name is the newsgroup that the classiﬁer thinks that the text string is “closest” to. It is computed using the classical kNN algorithm. This algorithm ﬁrst converts the input string into a TF-IDF vector (using the dictionary and count information computed over the original corpus). It then ﬁnds the k documents in the corpus that are “closest” to the query vector (where distance is computed using the L 2 norm), and returns the newsgroup label that is most frequent in those top k. Ties go to the label with the closest corpus document.
