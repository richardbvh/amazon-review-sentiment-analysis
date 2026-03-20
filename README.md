# Amazon Review Sentiment Analysis

This project applies **natural language processing (NLP)** and **machine learning** to classify Amazon customer reviews into **positive**, **neutral**, and **negative** sentiment categories.

Using cleaned review text data, the project compares different text representation methods and classification models to identify an effective approach for sentiment analysis. The final solution demonstrates how unstructured customer feedback can be transformed into structured insights for analysis and decision-making.

---

## Project Overview

Customer reviews contain valuable information about product experience, satisfaction, and service quality. However, review text is unstructured and difficult to analyse at scale without text processing techniques.

This project focuses on sentiment classification for Amazon reviews using NLP preprocessing and supervised machine learning. The work includes:

- data cleaning and preparation
- text preprocessing
- feature extraction
- model training and comparison
- evaluation of classification performance

---

## Project Objective

The objective of this project is to classify Amazon reviews into sentiment categories and compare the effectiveness of different text vectorisation methods and machine learning models.

The project aims to answer the following questions:

- How can customer review text be prepared for sentiment analysis?
- Which text representation method performs better for this dataset?
- Which classification model produces the strongest sentiment classification results?
- What limitations affect sentiment classification performance?

---

## Dataset

The project uses a sampled Amazon review dataset containing customer review text and associated sentiment labels.

After data cleaning, the dataset contained:

- **3,993 reviews**
- three sentiment classes:
  - **Positive**
  - **Neutral**
  - **Negative**

The class distribution was imbalanced, with positive reviews representing the majority of the dataset.

---

## Methods

### 1. Data Cleaning
The dataset was cleaned by:
- removing missing values
- removing duplicate records
- standardising text fields for processing

### 2. Text Preprocessing
Natural language preprocessing steps included:
- lowercasing
- tokenisation
- stopword removal
- lemmatisation
- punctuation and non-text cleaning
- negation handling (for example, preserving patterns such as `not good`)

### 3. Feature Extraction
Two text vectorisation methods were compared:

- **TF-IDF Vectorizer**
- **CountVectorizer**

### 4. Model Development
Two supervised machine learning models were trained and evaluated:

- **Multinomial Naive Bayes**
- **Linear Support Vector Machine (Linear SVM)**

---

## Models Compared

The project evaluated four modelling combinations:

1. **TF-IDF + Multinomial Naive Bayes**
2. **TF-IDF + Linear SVM**
3. **CountVectorizer + Multinomial Naive Bayes**
4. **CountVectorizer + Linear SVM**

These combinations were compared using classification performance metrics.

---

## Results

The model comparison showed the following results:

| Approach | Accuracy | Macro F1 Score |
|----------|----------|----------------|
| TF-IDF + Naive Bayes | 0.73 | 0.38 |
| TF-IDF + Linear SVM | 0.84 | 0.60 |
| CountVectorizer + Naive Bayes | 0.82 | 0.54 |
| CountVectorizer + Linear SVM | 0.82 | 0.59 |

### Best Performing Model
The strongest result was achieved by:

**TF-IDF + Linear SVM**
- **Accuracy:** 0.84
- **Macro F1 Score:** 0.60

---

## Key Findings

- **Linear SVM outperformed Multinomial Naive Bayes** on this sentiment classification task.
- **TF-IDF + Linear SVM** delivered the best overall performance.
- The **neutral** class was the hardest to classify accurately.
- Class imbalance affected model performance, especially for minority sentiment classes.
- NLP preprocessing and feature representation had a strong impact on classification quality.

---

## Business Relevance

This project shows how customer review text can be analysed to extract sentiment patterns from unstructured data.

Potential practical applications include:
- customer feedback monitoring
- product review analysis
- service quality assessment
- trend identification in consumer sentiment
- support for customer experience and business decision-making

---

## Tools and Technologies

- Python
- NLTK
- Scikit-learn
- Pandas
- NumPy
- Jupyter Notebook

---

## Repository Structure

```text
amazon-review-sentiment-analysis/
├── README.md
├── data/
├── notebooks/
└── docs/
