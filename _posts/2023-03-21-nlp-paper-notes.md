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

