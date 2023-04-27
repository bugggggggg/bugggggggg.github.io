---
title:  "Papers About Code Generation"
layout: post
---

## [CodeGeeX](https://arxiv.org/abs/2303.17568)

![language models related to programming languages](../assets/img/2023/2023-04-01-code-generation/img1.png)


## Meet in the Middle: A New Pre-training Paradigm
**great at code generation**

- a decoder-only transformer model trained both forward and backward.
    - next word prediction loss(forward)
    - previous word prediction loss(backward)
    - agreement loss(distance between forward and backward represetations of tokens)
- When inferring, synchronously generate tokens from both ends. (meet in the middle)