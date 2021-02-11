# Shapley values

**Tags**: data_science, feature_importance, shapley_values

**Author**: Dmitry Malkov, Data Monsters

![GitHub Logo](https://i.stack.imgur.com/lGb7V.png)

### Objective

Calculate the contribution of a specific feature to the overall prediction of the model

### Solution

Shapley numbers are perhaps the fairest way to calculate the [feature importance](https://github.com/ml-patterns/ml-patterns/blob/main/patterns/feature_importance_v1.md) for any model. This method considers the model as a game in which the features are the "players" and the outcome of the model is the common "prize". Shapley value is the average marginal contribution of a feature to the "prize" across all possible coalitions of "players". 

How to read the plot above:

Each point on the plot is a Shapley value for a feature and a data point. The position on the y-axis is determined by the feature and on the x-axis by the Shapley value. The color represents the value of the feature from low to high. Overlapping points are jittered in the y-axis direction, so we get a sense of the distribution of the Shapley values per feature. The features are ordered according to their importance.

### Links

[Interpretable Machine Learning Book](https://christophm.github.io/interpretable-ml-book/index.html)
