---
title: "11-424 Project 3: Epitran Support"
excerpt: "The third project for 11-424 Subword Modeling exploring G2P support."
collection: portfolio
---

## [11-424 Subword Modeling Project 3 Problem Statement](https://dmort27.github.io/subwordmodeling/assignments/project3.html): 

The goal of the third mini-project is to add G2P support for an unsupported language to Epitran or another, comparable framemork. In addition to adding support for the language, you must construct a set of unit tests that guarantee correct behavior of the module/model under varied conditions.

### My Approach: 
My primary sources for my mapping and processors were Omniglot, Wikipedia on Afrikaans, Wikipedia on Afrikaans phonology, Wikibooks on Afrikaans Pronunciation and A Grammar of Afrikaans by Bruce C. Donaldson.

I tried to create support for the main phonological changes that occur, but there seemed to be some degree of disagreement even between sources, so I tried to find the middle ground between them. The three most supported changes are word-final obstruent devoicing, sonorant merging, and (within the mapping) elongation of vowels. I am, however, not a native speaker and not very familiar with the language before this project so there was some difficulty. One of the variances that is not supported is phonological changes that correspond to syllabic structure as there seemed no straightforward method to apply changes without knowing the syllabic breakdown of the words as well as disagreement between sources on exact changes.

### Code Link: 
[Epitran Project](https://github.com/dmort27/epitran)  
