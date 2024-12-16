Word2Vec: Theoretical Background
This document provides a detailed explanation of the theoretical concepts behind Word2Vec, including its models, optimization techniques, and fundamental mathematical principles.
________________________________________
1. Introduction to Word2Vec
Word2Vec is a model that converts words into dense vector representations (word embeddings) to capture their contextual meaning. These embeddings can reveal semantic and syntactic relationships between words.
Word2Vec offers two core models:
•	Skip-gram
•	Continuous Bag of Words (CBOW)
________________________________________
2. Skip-gram Model
Objective:
•	Predict context words based on a target word.
Mathematical Representation:
The model maximizes the probability of observing a context word given a target word :
Optimization:
The probability is computed using the softmax function:
________________________________________
3. CBOW Model
Objective:
•	Predict the target word based on its surrounding context words.
Mathematical Representation:
The model maximizes the probability of a target word given its context :
________________________________________
4. Optimization Techniques
Word2Vec uses two key techniques to improve efficiency:
a. Negative Sampling
Instead of updating the probabilities of all words, only a small subset of "negative" words is sampled. This reduces computational costs.
b. Hierarchical Softmax
Constructs a binary tree for the vocabulary, reducing the computational complexity of the softmax function.
________________________________________
5. Semantic Rules
Orthogonality Rule (O Rule):
Unrelated words have orthogonal (or nearly orthogonal) vector representations:
Example: The vectors for "apple" and "quantum" are nearly orthogonal.
Clustering Rule (C Rule):
Similar words form clusters in the vector space:
Example: "king", "queen", and "royalty" form a semantic cluster.
________________________________________
6. Word Vector Arithmetic
Word embeddings support arithmetic operations to reveal relationships between words:
This property allows us to infer analogies and explore semantic relationships in the embedding space.
________________________________________
7. Reducing Dimensions
To visualize high-dimensional word vectors, dimensionality reduction techniques like PCA and t-SNE are used.
________________________________________
8. Combining Vectors
When two or more vectors represent similar concepts, they can be merged using:
1.	Summation: Combine element-wise:
2.	Weighted Combination: Adjust weights:
3.	Average Pooling: Compute element-wise average:
________________________________________
For practical examples and visualization, refer to the Notebook.

