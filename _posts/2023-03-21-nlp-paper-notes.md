---
title:  "NLP Paper Notes-2"
layout: post
---


-----
**Meet in the Middle: A New Pre-training Paradigm**
- a decoder-only transformer model trained both forward and backward.
    - next word prediction loss(forward)
    - previous word prediction loss(backward)
    - agreement loss(distance between forward and backward represetations of tokens)
- When inferring, synchronously generate tokens from both ends. (meet in the middle)

-----

**SELECTIVE ANNOTATION MAKES LANGUAGE MODELS BETTER FEW-SHOT LEARNERS**
- a method that helps to choose examples for in-context learning
    1. use SentenceBERT to put all samples into a vector space
    2. use cosine similarity and language model's confidence as metric to choose top-k samples
    3. manually annotate choosed samples
    4. when choosing examples for in-context learning, again use SentenceBERT to map the data into vector space and choose the k-nearest neighbors.

-----
**Parameter-Efficient Transfer Learning for NLP**

![Parameter-Efficient Transfer Learning for NLP](../assets/img/2023/2023-03-21-nlp-paper-notes/Parameter-Efficient%20Transfer%20Learning%20for%20NLP.png)

- add trainable **adapter** to pretrained transformer layers
- the parameters are initialized to near-zero. With the help of residual connection, the adapter is an approximate identical function(otherwise the training will fail) 

-----
