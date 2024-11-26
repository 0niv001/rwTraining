Classification is used to predict the likelihood of something being part of a category
Can be Binary or Multiclass. 

### Thresholding

The probability that we get from logistic regression can be converted into a binary value, that we can then use for classification

To map a logistic regression value to a binary category, we need to define a threshold - 1 or 0, but what about 0.6

Thresholds are problem dependent, and as such we need to tune their value.

Part of choosing a threshold is assessing how much we suffer from making a mistake.
