---
title:  "Papers About dataset of a LLM"
layout: post
---



## The Pile: An 800GB Dataset of Diverse Text for Language Modeling



## Deduplicating Training Data Makes Language Models Better
- About deduplicating training datasets.
- methods:
    - Exact match: use Suffix Array.
    - Approximate match: first use **MinHash**, then use 'edit distance' to further filter. Link similar documents. Any connected documents are considered as similar.

## The RefinedWeb Dataset for Falcon LLM: Outperforming Curated Corpora with Web Data, and Web Data Only