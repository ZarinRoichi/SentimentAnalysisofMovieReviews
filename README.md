# 🎬 Sentiment Analysis of Bengali Movie Reviews

## 📌 Overview
This project applies **Natural Language Processing (NLP)** and **transformer-based models** to classify Bengali movie reviews as **positive (0)** or **negative (1)**.  
We experimented with multiple transformer architectures (BanglaBERT, mBERT, XLM-R, Gemini) and fine-tuned them for Bengali sentiment classification.

---

## 🎯 Research Motivation
- Sentiment analysis helps businesses and researchers understand **public opinion**.  
- While English sentiment analysis is well-studied, **Bangla resources are scarce** despite being the 6th most spoken language in the world.  
- Challenges include:  
  - Informal expressions & spelling variations  
  - Dialect differences  
  - Code-mixed text (Bangla + English)  

This work aims to provide a **benchmark for Bengali movie review sentiment analysis**.

---

## ⚙️ Methodology
### Dataset
- **11,808 Bengali movie reviews** in CSV format  
- Two columns:  
  - `Reviews` → Bengali review text  
  - `Sentiment` → 0 (Positive), 1 (Negative)  

### Preprocessing
- Unicode filtering (Bengali characters only)  
- Text cleaning (symbols, punctuation, whitespace)  
- Normalization (spelling consistency)  
- Tokenization  
- Stopword removal  
- Label encoding (0/1)  

### Feature Extraction
- TF-IDF vectorizer (max vocab = 5000)  
- Transformer embeddings for context-aware representation  

### Classification
- Fine-tuned models:  
  - **BanglaBERT**  
  - **mBERT**  
  - **XLM-RoBERTa (XLM-R)**  
  - **Gemini**  

---

## 📊 Results

| Model       | Accuracy | Precision | Recall | F1-score |
|-------------|----------|-----------|--------|----------|
| **BanglaBERT** | **97.16%** | 95.67 | 94.41 | 95.04 |
| XLM-R       | 91.40%   | 87.20    | 82.20  | 84.63 |
| mBERT       | 90.22%   | 90.19    | 90.22  | 90.20 |
| Gemini      | 72.03%   | 75.57    | 73.03  | 63.92 |

### Key Insights
- **BanglaBERT performed best** with ~97% accuracy and strong precision-recall balance.  
- **XLM-R and mBERT** provided competitive results (~90–91% accuracy).  
- **Gemini underperformed** (72%), showing limitations for this domain.  
- Transformer-based models significantly outperform classical ML approaches for Bangla sentiment tasks.  

---

## 🚀 Future Work
- Incorporate **FastText embeddings** and larger Bangla pretraining corpora.  
- Improve **Gemini performance** with better fine-tuning strategies.  
- Address **class imbalance** with oversampling/undersampling methods.  
- Expand dataset with reviews from **news & social media**.  
- Deploy a **real-time web or mobile app** for Bangla sentiment analysis.  

---

