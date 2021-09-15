# Product recommendation system based on text customer reviews

**Solution by**: [MIL Team](https://machine-intelligence.ru/en/about)

**Date**: September 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/Product_recommendation_system based_on_text_customer_reviews.jpeg)

### Challenge

The information from users’ reviews is useful for building recommendation systems. However, it is difficult to extract it automatically.

### Solution

A semi-automatic method of extracting terms from text in question was applied, and a knowledge graph was built. Extracted terms were associated with the technical characteristics of the goods. Vector representations of the graph elements were trained which significantly improved the quality of the recommendations.

Technologies used:
- Adaptive Text Rank based on technical characteristics and a set of sentiment words
- SOTA BERT model for matching terms and technical characteristics of the goods
- TransE method for training vector representations of graph elements
- ABAE method for highlighting important characteristics for products from a set of reviews

### Technologies

Python, Tensorflow
