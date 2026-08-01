# 📝 Customer Review Topic Modeling

A Natural Language Processing (NLP) project that explores **unsupervised topic modeling** techniques to discover latent themes from customer reviews. The project implements both **traditional probabilistic topic modeling** using **Latent Dirichlet Allocation (LDA)** and **modern embedding-based topic modeling** using **BERTopic**, enabling a comprehensive comparison between classical and transformer-based approaches.

---

## 📌 Overview

Customer reviews contain valuable insights into user opinions, product quality, customer satisfaction, and recurring issues. However, manually analyzing thousands of reviews is time-consuming and impractical.

This project develops an end-to-end NLP workflow that automatically identifies hidden topics within customer reviews using two complementary approaches:

* **LDA (Latent Dirichlet Allocation)** for probabilistic topic discovery based on word distributions.
* **BERTopic** for semantic topic extraction using transformer embeddings and density-based clustering.

The entire workflow is implemented in **Google Colab**, allowing experiments to be performed without requiring a local machine setup.

---

## 🎯 Objectives

* Extract meaningful latent topics from customer reviews.
* Compare classical and transformer-based topic modeling techniques.
* Perform comprehensive text preprocessing for improved topic quality.
* Visualize discovered topics and their relationships.
* Identify recurring themes and customer concerns from large review datasets.

---

## 📂 Dataset

The project is designed to work with customer review datasets collected from sources such as product feedback.

Each record typically contains:

* Customer review text
* Optional metadata (sentiment)

---

## 🔤 NLP Preprocessing Pipeline

The reviews undergo multiple preprocessing steps before topic modeling.

### Text Cleaning

* Lowercase conversion
* Removal of punctuation
* Removal of numbers
* Removal of special characters
* Stop-word removal

### Tokenization

* Word tokenization
* Lemmatization
* Corpus construction
* Dictionary generation

### Phrase Detection

To capture meaningful expressions, the workflow generates:

* Bigrams
* Trigrams

Examples:

* "customer service"
* "battery life"
* "delivery time"

### TF-IDF Based Filtering

Frequently occurring but less informative words are filtered using TF-IDF, improving topic coherence and reducing noise before model training.

---

## 🏗️ Topic Modeling Approaches

### 1. Latent Dirichlet Allocation (LDA)

The classical topic modeling pipeline includes:

* Text preprocessing
* Dictionary creation
* Bag-of-Words representation
* TF-IDF filtering
* LDA topic modeling
* Topic interpretation

LDA identifies topics by learning probability distributions over words and documents.

---

### 2. BERTopic

A semantic topic modeling workflow is implemented using modern transformer embeddings.

Pipeline:

```text id="rnlm6v"
Customer Reviews
        │
        ▼
Sentence Transformer Embeddings
        │
        ▼
UMAP Dimensionality Reduction
        │
        ▼
HDBSCAN Clustering
        │
        ▼
BERTopic
        │
        ▼
Semantic Topics
```

The BERTopic workflow consists of:

* Sentence Transformer embeddings
* UMAP for dimensionality reduction
* HDBSCAN for density-based clustering
* BERTopic for semantic topic extraction and representation

This approach captures semantic similarity beyond simple word frequency, enabling more coherent and meaningful topic discovery.

---

## 📊 Visualization

The project includes visualizations to aid topic interpretation and analysis.

### LDA Visualizations

* Topic keyword distributions
* Topic-word probabilities
* **Intertopic Distance Map** for understanding relationships between discovered topics

### BERTopic Visualizations

* Topic representations
* Topic frequency analysis
* Semantic topic exploration
* Interactive topic visualizations

---

## ☁️ Google Colab

The complete workflow is implemented in **Google Colab**, making it easy to reproduce experiments without local installation.

**Google Colab Notebook:**

> *Add Google Colab link here.*

---

## 📈 Results

The implemented workflows successfully demonstrate:

* End-to-end NLP preprocessing
* Automatic latent topic extraction
* Phrase detection using bigrams and trigrams
* Noise reduction using TF-IDF filtering
* Probabilistic topic discovery with LDA
* Semantic topic discovery with BERTopic
* Interactive visualization of discovered topics

---

## 🛠 Technologies Used

* Python
* Gensim
* LDA (Latent Dirichlet Allocation)
* BERTopic
* Sentence Transformers
* UMAP
* HDBSCAN
* TF-IDF
* Google Colab

---

## 🚀 Applications

* Customer Feedback Analysis
* Product Review Mining
* Market Research
* Opinion Mining
* Business Intelligence
* Brand Monitoring
* Product Improvement
* Social Media Analytics
* Survey Analysis

---

## 🔮 Future Improvements

Potential enhancements include:

* Dynamic topic modeling for time-based trend analysis
* Automatic topic labeling using Large Language Models (LLMs)
* Sentiment-aware topic modeling
* Multilingual topic modeling
* Interactive dashboards for topic exploration
* Integration with real-time review streams
* Comparative evaluation using topic coherence metrics

---

## 🙏 Acknowledgements

This project builds upon several outstanding open-source libraries and research contributions from the NLP community.

Special thanks to the developers and maintainers of:

* **Gensim** for classical topic modeling and LDA implementations.
* **BERTopic** for transformer-based semantic topic modeling.
* **Sentence Transformers** for high-quality sentence embeddings.
* **UMAP** for nonlinear dimensionality reduction.
* **HDBSCAN** for density-based clustering.
* **Google Colab** for providing accessible cloud-based GPU resources that enabled development and experimentation.

---

## 📈 Summary

This project presents a comprehensive NLP workflow for **customer review topic modeling**, combining **classical probabilistic modeling (LDA)** with **modern semantic topic modeling (BERTopic)**. Through extensive preprocessing, phrase detection, TF-IDF filtering, transformer embeddings, dimensionality reduction, clustering, and visualization, the project demonstrates effective extraction of latent themes from customer reviews. Implemented entirely in **Google Colab**, the workflow provides a reproducible and accessible framework for large-scale review analysis and business insight generation.
