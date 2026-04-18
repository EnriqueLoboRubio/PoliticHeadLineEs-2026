# Hybrid Political News Ranking System (PoliticHeadlinesES 2026)

This repository contains the implementation of a hybrid ranking system developed for **Task 1 of PoliticHeadlinesES 2026 (IberLEF)**.

The approach combines **lexical methods** (TF-IDF and word overlap) with a **bi-encoder model** to capture both term-based and semantic similarities between news headlines and article bodies.

---

## ⚙️ Method

The system follows a hybrid pipeline:

1. Pair generation (body–headline)
2. Similarity computation:
   - TF-IDF
   - Word overlap
   - Bi-encoder embeddings
3. Score normalization (min-max)
4. Weighted combination of signals
5. Ranking of candidates
