---
title: "11-424 Project 1: Morphological Segmentation"
excerpt: "The first project for 11-424 Subword Modeling exploring morphological segmentation."
collection: portfolio
---

## [11-424 Subword Modeling Project 1 Problem Statement](https://dmort27.github.io/subwordmodeling/assignments/project1.html): 

The goal of the first project is to develop a tokenizer—a morphological segmenter—that segments text from an arbitrary language more similarly to gold morpheme segmentations by a linguist than two baselines: a Morfessor baseline and a Unigram tokenization model.

### My Approach: 
Following several different attempts at different approaches, I finally settled on approaching the problem of creating a BPE model with improved vocabulary size selection. I used the Hugging Face BPE model and trained it on the morphemes present in the train and dev datasets for both languages. For Rarámuri, I tried manually finding a decent vocabulary size that would edge out the baselines, but it took quite a while. I then implemented part of the VOLT algorithm (Source 1) to write an algorithm that would generate the optimal size of the vocabulary. I then retrained my BPE model on that vocabulary size and saw an improvement in f1 scores. For the final test data, I inflated the vocabulary size by 100 tokens (roughly the size of the dataset in each case to account for if each word was a completely foreign morpheme not seen previously in the grammar) to account for previously unseen elements in the new data.

### Code Link: 
[Project 1 Code](https://colab.research.google.com/drive/18nEe8y3mJJCR434kKRWRegPrw7_eVQzM?usp=sharing)  

### Source 1: 
Jingjing Xu, Hao Zhou, Chun Gan, Zaixiang Zheng, and Lei Li. 2021. Vocabulary Learning via Optimal Transport for Neural Machine Translation. In Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers), pages 7361–7373, Online. Association for Computational Linguistics
