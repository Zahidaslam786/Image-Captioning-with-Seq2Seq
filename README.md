# Image-Captioning-with-Seq2Seq

A multimodal deep learning model that generates natural language descriptions for images using a Sequence-to-Sequence (Seq2Seq) architecture. This project was developed as Assignment 1 for the **Generative AI** course at **FAST-NUCES**.

---

## 🚀 Project Overview
This project implements a "Neural Storyteller" capable of understanding visual scenes and translating them into human-readable text. It bridges the gap between Computer Vision and Natural Language Processing (NLP) using the **Flickr30k Dataset**.



---

## 🏗️ Model Architecture

### 1. Encoder (Feature Extraction)
* [cite_start]**Pre-trained Model:** ResNet50[cite: 27, 61].
* [cite_start]**Logic:** The final classification layer was removed to "cache" images into 2048-dimensional feature vectors[cite: 27, 81].
* [cite_start]**Optimization:** Image features are saved into a `flickr30k_features.pkl` file to avoid expensive re-computation during training[cite: 26, 28].

### 2. Decoder (Sequence Generation)
* [cite_start]**Architecture:** LSTM-based Recurrent Neural Network[cite: 83].
* [cite_start]**Input:** Word Embeddings of captions concatenated with image features[cite: 84, 86].
* [cite_start]**Vocabulary:** Built from `captions.txt` with a frequency threshold to ensure robust learning[cite: 78].

---

## 📈 Performance Metrics
The model was evaluated using standard NLP metrics to ensure caption quality:

* **BLEU-4 Score:** 0.0773
* **Precision:** 0.4124
* **Recall:** 0.3311
* **F1-Score:** 0.3527



---

## 🛠️ Key Features
* [cite_start]**Dual Inference Methods:** Supports both **Greedy Search** and **Beam Search** (k=3) for generating captions[cite: 90].
* [cite_start]**Data Pre-processing:** Automated text cleaning and tokenization pipeline[cite: 78].
* [cite_start]**Interactive App:** Integrated with **Gradio** for real-time image upload and captioning[cite: 101].

---

## 💻 Environment Setup
* [cite_start]**Platform:** Kaggle / Google Colab[cite: 22].
* [cite_start]**Accelerator:** GPU T4 x2 (Dual GPU)[cite: 23].
* [cite_start]**Dataset:** [Flickr30k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr30k)[cite: 24].

---

## 📂 Deliverables
1. [cite_start]**Model Notebook:** Complete `.ipynb` file named `AI_ASS01_22F_3394`[cite: 13].
2. [cite_start]**Loss Curve:** Plot showing training progress over epochs[cite: 95, 96].
3. [cite_start]**App Deployment:** Streamlit/Gradio application link[cite: 101].

---

**Developed by:** Muhammad Zahid Aslam  
**Student ID:** 22F-3394  
**University:** National University of Computer and Emerging Sciences (FAST-NUCES)
