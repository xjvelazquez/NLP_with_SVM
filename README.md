# NLP_with_SVM
A common approach to analyzing text data is to use methods that allow us to convert text data into some kind of numerical representation - since we can then use all of our mathematical tools on such data. In this assignment, we will explore 2 feature engineering methods that convert raw text data into numerical vectors:

Bag of Words (BoW)
BoW encodes an input sentence as the frequency of each word in the sentence.
In this approach, all words contribute equally to the feature vectors.

Term Frequency - Inverse Document Frequency (TF-IDF)
TF-IDF is a measure of how important each term is to a specific document, as compared to an overall corpus.
TF-IDF encodes a each word as the it's frequency in the document of interest, divided by a measure of how common the word is across all documents (the corpus).
Using this approach each word contributes differently to the feature vectors.
The assumption behind using TF-IDF is that words that appear commonly everywhere are not that informative about what is specifically interesting about a document of interest, so it is tuned to representing a document in terms of the words it uses that are different from other documents.

To compare those 2 methods, we will first apply them on the same Movie Review dataset to analyse sentiment (how positive or negative a text is). In order to make the comparison fair, the same SVM (support vector machine) classifier will be used to classify positive reviews and negative reviews.

SVM is a simple yet powerful and interpretable linear model. To use it as a classifier, we need to have at least 2 splits of the data: training data and test data. The training data is used to tune the weight parameters in the SVM to learn an optimal way to classify the training data. We can then test this trained SVM classifier on the test data, to see how well it works on data that the classifier has not seen before.
