---
title: "11-424 Project 2: Reinflection & Paradigm Completion"
excerpt: "The second project for 11-424 Subword Modeling exploring reinflection and paradigm completion."
collection: portfolio
---

## 11-424 Subword Modeling Project 2 Problem Statement: 

The goal of the second project is to generate the inflectional forms of verbs for Karbardian (kbd), Swahili (swc), and Mixtec (sty) from roots + inflectional information better than non-neural and neural baselines.

### My Approach: 
My approach was to implement post-processing on the non-neural baseline. For KBD, I attempted to fix the learning of incorrect morphemes. For SWC, I attempted to fix for the unknown reinflection element causing duplicates in the training data as well as manually implement the rules for adjectives. For XTY, I again attempted to fix the incorrect learning of morphemes as well as clean up issues with punctuation within the data. 

### Code Link: 
[Project 2 Code](https://colab.research.google.com/drive/1Sw3JqCTl0JRmryYMjvH05-AI8sKeHc7F#scrollTo=4JI36ZMil_dp)  
