This repository contains two comprehensive Information Retrieval (IR) projects aimed at exploring and evaluating the core principles of search engines: a **Text-based Search System** using the Cranfield Collection and a **Prototype Image Search Engine** mimicking early Google Image Search capabilities.

---

## 📚 Project 1: Text-Based Information Retrieval (Cranfield Collection)

### 🔍 Overview
This project focuses on implementing and evaluating an Information Retrieval system using the **Cranfield Collection**, which contains 1,400 abstracts and associated queries. The goal is to explore different retrieval models and evaluate their effectiveness using standard IR metrics.

### 📌 Objectives
- Preprocess and index a corpus of documents
- Implement three retrieval models:
  - Vector Space Model (TF-IDF)
  - BM25
  - Query Likelihood (Language Model)
- Evaluate the models using:
  - **Mean Average Precision (MAP)**
  - **Precision@5 (P@5)**
  - **Normalized Discounted Cumulative Gain (NDCG)**

### ⚙️ Methodology
1. **Indexing**
   - Tokenization, stopword removal, and normalization
   - Inverted index construction
2. **Retrieval Models**
   - Implemented in Python with custom scoring functions
3. **Evaluation**
   - TREC-style evaluation setup
   - Ground truth relevance judgments used for metric calculations

### 📈 Insights
The project compares the performance of the three models and discusses their relative strengths and weaknesses. It also explores the impact of retrieval assumptions and preprocessing on performance.

---

## 🖼️ Project 2: Prototype Image Search Engine

### 📷 Overview
This project implements a lightweight image search engine inspired by early versions of **Google Image Search**. It consists of image crawling, feature extraction, indexing, and a web-based retrieval interface.

### 📌 Objectives
- Scrape and collect labeled images from [Pexels](https://www.pexels.com)
- Generate image surrogates using:
  - **Alt-text** (HTML annotations)
  - **ResNet-50 CNN features**
- Build a retrieval pipeline using:
  - **TF-IDF vectorization**
  - **Cosine similarity**
- Develop a web-based interface for querying and displaying results

### ⚙️ System Architecture
- **Image Collection**: Python-based web scraper
- **Feature Extraction**:
  - Alt text from HTML
  - Deep feature extraction using pretrained ResNet-50
- **Indexing**: Vectorized representations using TF-IDF
- **Retrieval**: Rank images using cosine similarity against query terms
- **Frontend**: HTML + Flask web interface for user input and results display

### 📈 Evaluation
Search engine performance is evaluated based on:
- **Query relevance**
- **Image diversity**
- **User satisfaction feedback**

---

## 💻 Technologies Used
- Python (scikit-learn, Flask, NumPy, pandas)
- ResNet-50 (via PyTorch/TensorFlow for feature extraction)
- TREC Eval tools (for Cranfield evaluation)
- HTML/CSS for frontend
