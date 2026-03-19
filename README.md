# 🧠 LLM Corpus Preparation

A hands-on repository focused on **data sampling, cleaning, and tokenization strategies** for Large Language Models (LLMs).

This work explores how different preprocessing and encoding techniques impact text representation before feeding data into transformer-based architectures.

---

##  Overview

Before training any LLM, raw text must go through several preparation steps.
This repository implements and compares these steps in a modular and reproducible way.

The goal is to:

* Understand **data preprocessing pipelines**
* Experiment with **different tokenization methods**
* Analyze how encoding choices affect downstream modeling

---

##  General Pipeline

The workflow followed in this repository:

```
Raw Text
   ↓
Data Cleaning
   ↓
Normalization
   ↓
Data Sampling / Filtering
   ↓
Tokenizer Training (BPE / WordPiece / Unigram)
   ↓
Text → Tokens → Token IDs
   ↓
(Ready for LLM input pipeline)
```

---

## Data Preparation

### 1. Cleaning

Basic preprocessing applied to raw text:

* Remove or replace newline characters
* Normalize whitespace
* Handle special patterns (e.g., `--`)
* Optional removal of noisy symbols

### 2. Normalization

* UTF-8 consistency
* Whitespace standardization
* Text formatting cleanup

### 3. Sampling & Filtering

* Remove very short or low-quality samples
* Deduplication (optional)
* Dataset balancing (if applicable)

---

## Tokenization / Encoding Methods

This repository focuses on **subword tokenization techniques**, which balance vocabulary size and representation power.

### 1. Byte Pair Encoding (BPE)

* Iteratively merges frequent character pairs
* Widely used in GPT-style models
* Efficient and deterministic

---

### 2. WordPiece

* Used in models like BERT
* Similar to BPE but based on likelihood
* Optimized for probabilistic token selection

---

### 3. Unigram Language Model

* Used in SentencePiece
* Starts with a large vocabulary and removes tokens based on probability
* More flexible and probabilistic than BPE

---

### 4. Byte-Level BPE

* Variant of BPE operating on byte sequences
* Handles any input text (including emojis and rare symbols)
* Used in modern GPT models

---

## Experimentation Goals

This repo enables comparison across:

* Different tokenizers (BPE vs WordPiece vs Unigram)
* Different cleaning strategies
* Vocabulary size vs sequence length trade-offs

Evaluation metrics:

* Token distribution
* Vocabulary efficiency
* Average sequence length
* Coverage of rare words

---


## Contributions

Feel free to fork, experiment, and improve the pipeline.
This project is designed to be modular and extensible.

---

## Note

This repository focuses **only on data preparation and tokenization**, not on model training.

---

## star If you find this useful

Give it a star — it helps others discover the project!

#### by Amirtha Ganesh R (one step towards making ai feasible to all)
