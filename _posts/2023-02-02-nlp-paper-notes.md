---
title:  "NLP Paper Notes"
layout: post
---

-----

**PromptCap: Prompt-Guided Task-Aware Image Captioning**
- use few-shot learning to synthesize training data from large language models. Then filter the data to ensure the quality.

-----

**A parallel corpus of Python functions and documentation strings for automated code documentation and code generation**

- a [dataset](https://github.com/EdinburghNLP/code-docstring-corpus) of 300,000 python functions and docstrings
- release python script of scraping Github public resporitories
- [a python scraper](https://github.com/uclnlp/pycodesuggest)

-----
**AlphaCode**
- pretrain on Github, finetuning on [CodeContest Dataset](https://github.com/deepmind/code_contests)
- Transformer decoder-encoder: encoder uses masked prediction and decoder uses next token prediction
- sample millions programs from model, then filter and cluster

-----
**BERT**
- transformer encoder pretrained with masked token prediction and next sentence prediction

-----
[x]**Language Models are Few-Shot Learners(GPT3)**

-----