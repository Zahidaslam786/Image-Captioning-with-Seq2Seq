# Image-Captioning-with-Seq2Seq

A multimodal deep learning model that generates natural language descriptions for images using a Sequence-to-Sequence (Seq2Seq) architecture. This project was developed as Assignment 1 for the **Generative AI** course at **FAST-NUCES**.

---

## 🚀 Project Overview
This project implements a "Neural Storyteller" capable of understanding visual scenes and translating them into human-readable text. It bridges the gap between Computer Vision and Natural Language Processing (NLP) using the **Flickr30k Dataset**.



---

## 🏗️ Model Architecture

### 1. Encoder (Feature Extraction)
* **Pre-trained Model:** ResNet50.
* **Logic:** The final classification layer was removed to "cache" images into 2048-dimensional feature vectors.
* **Optimization:** Image features are saved into a `flickr30k_features.pkl` file to avoid expensive re-computation during training.

### 2. Decoder (Sequence Generation)
* **Architecture:** LSTM-based Recurrent Neural Network.
* **Input:** Word Embeddings of captions concatenated with image features.
* **Vocabulary:** Built from `captions.txt` with a frequency threshold to ensure robust learning.

---

## 📈 Performance Metrics
The model was evaluated using standard NLP metrics to ensure caption quality:

* **BLEU-4 Score:** 0.0773
* **Precision:** 0.4124
* **Recall:** 0.3311
* **F1-Score:** 0.3527

<img width="855" height="470" alt="image" src="https://github.com/user-attachments/assets/4a87255e-d767-4d9a-809d-24216f722b1b" />


---

## 🛠️ Key Features
* **Dual Inference Methods:** Supports both **Greedy Search** and **Beam Search** (k=3) for generating captions.
* **Data Pre-processing:** Automated text cleaning and tokenization pipeline.
* **Interactive App:** Integrated with **Gradio** for real-time image upload and captioning.

---

## 💻 Environment Setup
* **Platform:** Kaggle / Google Colab.
* **Accelerator:** GPU T4 x2 (Dual GPU).
* **Dataset:** [Flickr30k Dataset](https://www.kaggle.com/datasets/adityajn105/flickr30k).

<img width="1305" height="589" alt="image" src="https://github.com/user-attachments/assets/d671d0d1-de26-4dc7-9fb5-161a0ce712fd" />

<img width="1309" height="597" alt="image" src="https://github.com/user-attachments/assets/66aa1713-042a-4085-8791-8f03a82079af" />

<img width="593" height="433" alt="image" src="https://github.com/user-attachments/assets/b941d09a-388d-4612-9d5d-214ffa8f0b93" />

---

**Developed by:** Muhammad Zahid Aslam  
**Student ID:** 22F-3394  
**University:** National University of Computer and Emerging Sciences (FAST-NUCES)
