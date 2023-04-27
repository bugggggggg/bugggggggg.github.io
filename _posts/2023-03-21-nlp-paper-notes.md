---
title:  "NLP Paper Notes-2"
layout: post
---

## SELECTIVE ANNOTATION MAKES LANGUAGE MODELS BETTER FEW-SHOT LEARNERS
- a method that helps to choose examples for in-context learning
    1. use SentenceBERT to put all samples into a vector space
    2. use cosine similarity and language model's confidence as metric to choose top-k samples
    3. manually annotate choosed samples
    4. when choosing examples for in-context learning, again use SentenceBERT to map the data into vector space and choose the k-nearest neighbors.


## Parameter-Efficient Transfer Learning for NLP

![Parameter-Efficient Transfer Learning for NLP](../assets/img/2023/2023-03-21-nlp-paper-notes/Parameter-Efficient%20Transfer%20Learning%20for%20NLP.png)

- add trainable **adapter** to pretrained transformer layers
- the parameters are initialized to near-zero. With the help of residual connection, the adapter is an approximate identical function(otherwise the training will fail) 


## Scaling Transformer to 1M tokens and beyond with RMT
- RMT: recurrent memory transformer
- curriculum learning: first converge on simple problems and iteratively increase the difficulty
- In RNN, every unit takes one token. In RMT, we can view every unit as a transformer block.

![1](../assets/img/2023/2023-03-21-nlp-paper-notes/Scaling%20Transformer%20to%201M%20tokens%20and%20beyond%20with%20RMT.png)


## Dataset Cartography: Mapping and Diagnosing Datasets with Training Dynamics
- A method to estimate data quality
    - During training process, we record the confidence of the gold label for every training record in every epoch.
    - Calculate the mean and variability for every record
    - Every record can be clasified into one of the three fields
    ![1](../assets/img/2023/2023-03-21-nlp-paper-notes/Dataset%20Cartography.png)


