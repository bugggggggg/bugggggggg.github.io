---
title: "literature review p1"
layout: post
---


### 20240325
**LLM2LLM: Boosting LLMs with Novel Iterative Data Enhancement**

propose a data augmentation method for LLM finetune. 

1. start from a seed dataset, finetune student model on it.
2. evaluate on train set, find wrong cases. 
3. Annotate wrong cases with teacher model
4. Append the annotated data to seed dataset and go step 1


**Cobra: Extending Mamba to Multi-Modal Large Language Model for Efficient Inference**

- Mamba as llm backbone for vision-language model. 
- Combine DINOv2 and SigLIP feature as vision feature
- MLP for alignment module


**MATHVERSE: Does Your Multi-modal LLM Truly See the Diagrams in Visual Math Problems?**

In math VLM benchmarks like MathVista, GeoQA, etc, the text contains redundant information, so it might not accurately reveal the model's visual reasoning ability
propose MATHVERSE benchmark,


### 20240326

**Data Mixing Laws: Optimizing Data Mixtures by Predicting Language Modeling Performance**

propose data mixing scaling law, get optimal data mixing
similar to regression on small runs(small data, model and steps)

experiments are only on 1B models

**RakutenAI-7B: Extending Large Language Models for Japanese**

7B llm for Japanese


### 20240401

**Are We on the Right Way for Evaluating Large Vision-Language Models?**

LVLMs do well on current benchmarks even without visual information(images)

propose MMStar benchmark by sampling from existing benchmarks and filtering(llm accuracy followed with manual filtering)


### 20240402

**Unsolvable Problem Detection: Evaluating Trustworthiness of Vision Language Models**

Based on MMbench, propose a benchmark in which the problem is unsolvable.

**Visual Goal-Step Inference using wikiHow**

The wikiHow dataset contains a high-level goal (how to do something) accompanied by interleaved images and text representing the steps.

the task in the paper is to match the goal with images.


### 202405
**LLaVAR: Enhanced Visual Instruction Tuning for Text-Rich Image Understanding**

Select text-rich images from laion.
Use "ocr result", "caption" as context to generate QA pairs with GPT-4. 
Fine-tune llava


**Odyssey-Math**

A hard math benchmark(harder than Math and GSM8K)
ask model to generate json format ({"answer": "", "reasoning": ""}), then use LLM to judge the answer with std
cons:
- it's better to put the "reasoning" first. 
- why json format? it's better output answer then judged with LLM like MathVista
