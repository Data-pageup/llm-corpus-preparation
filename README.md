# 🧠 LLM Corpus Preparation

A hands-on repository focused on **data sampling, cleaning, and tokenization strategies** for Large Language Models (LLMs).

### so here we go with this flow. 

First method :
text data. -> little bit cleaning( by removing unwanted characters) -> then using byte pair encoding -> token embeddings ( by using neural net to optimise the weights ) -> positional embeddings ( same as token embeddings) -> input embeddings ( token embedding + positional embedding)

Second method :

text data -> cleaning -> using bert/ word2vec  tokenizer for token embeddings -> positional embeddings -> input - output pair .

we will be training with word 2 vec and also bert transformer

