# Feature importance

**Tags**: data_science

**Author**: Dmitry Malkov, Data Monsters

![GitHub Logo](https://progi.pro/media/main/4d/a7/34/4da73418da5e7bbb50fb3cec58f7846d.png)

### Objective

Calculate the contribution of a specific feature to the overall prediction of the model

### Solution

For some types of models, such as linear and logistic regression and decision trees, there are special fast and well-interpreted methods.

There are also model-agnostic methods that treat a model as a black box and use only information about its inputs and predictions. The most theoretically justified and stable method is the Shapley values method, which, however, is computationally expensive. Permutation and local surrogate interpretable model methods are also often used.

### Links

[Interpretable Machine Learning Book](https://christophm.github.io/interpretable-ml-book/index.html)
