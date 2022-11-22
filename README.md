# Naive-Bayes-classifier
# <b> <u>Introduction: What is Naive Bayes Classifier? </u></b>
![image](https://user-images.githubusercontent.com/102477662/203233484-b370d9e0-abed-49be-bfb1-231dad202e02.png)


Naive Bayes models are a group of extremely fast and simple classification algorithms that are often suitable for very high-dimensional datasets. Because they are so fast and have so few tunable parameters, they end up being very useful as a quick-and-dirty baseline for a classification problem.


Naive Bayes classifiers are built on Bayesian classification methods. These rely on Bayes's theorem, which is an equation describing the relationship of conditional probabilities of statistical quantities. In Bayesian classification, we're interested in finding the probability of a label given some observed features, which we can write as P(L | features). Bayes's theorem tells us how to express this in terms of quantities we can compute more directly:

### $P(L ~|~ \rm features)=\frac{P(\rm features ~|~ L) P(L)}{P(\rm features)}$

If we are trying to decide between two labels—let's call them $L_1$ and $L_2$—then one way to make this decision is to compute the ratio of the posterior probabilities for each label:

# $\frac{P(L_1 ~|~ \rm features)}{P(L_2 ~|~ \rm features) }= \frac{P(\rm features ~|~ L_1)}{P(\rm features ~|~ L_2)}\frac{P(L_1)}{P(L_2)}$

All we need now is some model by which we can compute $P(\rm features~|~ L)$ for each label. Such a model is called a generative model because it specifies the hypothetical random process that generates the data. Specifying this generative model for each label is the main piece of the training of such a Bayesian classifier. The general version of such a training step is a very difficult task, but we can make it simpler through the use of some simplifying assumptions about the form of this model.

### The posterior probability can be written as : 

# $P(Y ~|~X) = P(y)P(x_1|y)P(x_2|y,x_1)....P(x_n|y,x_1,...,x_{n-1})$

### Assuming all the X are conditionally independent
# $P(Y=1|X) = \frac{P(y=1)P(x_1|y=1)....P(x_n|y=1)}{P(X)}$

This is where the "naive" in "naive Bayes" comes in: if we make very naive assumptions about the generative model for each label, we can find a rough approximation of the generative model for each class, and then proceed with the Bayesian classification. Different types of naive Bayes classifiers rest on different naive assumptions about the data, and we will examine a few of these in the following sections.
