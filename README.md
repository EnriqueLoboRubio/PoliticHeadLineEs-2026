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

## 📦 Data & Model Requirements

This repository does not include the datasets used in the competition.

To run the system, the **development and evaluation datasets from PoliticHeadlinesES 2026** must be downloaded manually from the official competition sources and placed in the appropriate directory (e.g., `/data/`).

Due to licensing restrictions, these datasets are not redistributed in this repository.

---

### 🤖 Model

The system uses the following bi-encoder model:

- `sentence-transformers/paraphrase-multilingual-mpnet-base-v2`

This model is **automatically downloaded** the first time the code is executed using the Sentence Transformers library, so no manual setup is required.

Make sure you have an active internet connection on first run to allow the model to be retrieved.
