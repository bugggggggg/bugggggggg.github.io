---
title:  "NLP Paper Notes"
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


