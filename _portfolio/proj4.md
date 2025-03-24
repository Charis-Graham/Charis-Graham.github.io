---
title: "11-424 Project 4: Cognate Detection"
excerpt: "The fourth project for 11-424 Subword Modeling exploring cognate detection."
collection: portfolio
---

## [11-424 Subword Modeling Project 4 Problem Statement](https://dmort27.github.io/subwordmodeling/assignments/project4.html): 

Cognates are pairs of words that are descended from the same word in an language directly ancestral to the two languages from which the pairs are drawn. These are to be distinguished from loanwords (or borrowings), which are “borrowed” into one language from a another language. Borrowing is like adoption and the relationship between cognates is like tha between blood siblings.

In this project, you will build a model to automatically identify cognates.

### My Approach: 
My approach was fairly straightforward. I used a BERT-backend sentence transformer model that uses CLI to pool vector representations of the words in the definitions into one vector embedding representing each definition. I then used Euclidean distance to find the 10 closest cognate definition vectors to the input words for Ukhrul for both Kaichi and Tusom. Then I used Levenshtein distance to calculate the number of character swaps I would need to do to go from the input word in Ukhrul to each of its top 10 suggested cognates. I then generated a score of 0.75*(Euclidean distance) + 0.25*(Levenshtein distance). I then found the top 5 scorers and used those as my top five candidates. 

### Code Link: 
[Project 4 Code](https://drive.google.com/file/d/1PjEdwsSXsE1_55mU-ev_Y3s_xdyeqOtU/view?usp=sharing)  
