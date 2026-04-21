# 🖼️ Image Captioning using VGG16 + LSTM + Attention

This project implements an **Image Captioning System** that automatically generates human-like descriptions for images using Deep Learning.  
It follows the **“Show, Attend and Tell” architecture**, combining **Computer Vision (CNN)** and **Natural Language Processing (NLP)**.

---

## 📌 Features
- Extracts image features using **VGG16 (pre-trained on ImageNet)**
- Uses **LSTM decoder** to generate captions word-by-word
- Applies **Bahdanau Attention mechanism** to focus on important image regions
- Trained and evaluated on the **Flickr8k dataset**
- Produces accurate and human-like image descriptions

---

## 🧠 Architecture Overview

### 🔹 Encoder (CNN)
- Pre-trained **VGG16 model** (without top layers)
- Extracts deep visual features from images
- Outputs a fixed-length feature vector representing image content

### 🔹 Decoder (RNN)
- **Embedding Layer → LSTM → Dense Layer**
- Generates captions sequentially word by word
- Uses image features + previous words as input

### 🔹 Attention Mechanism
- Focuses on relevant parts of the image at each time step
- Improves caption quality and interpretability
- Helps the model attend to important regions while generating words

---

## 🗂️ Dataset
- **Flickr8k Dataset**
  - 8,000 images
  - Used for training and evaluation
---
### ⚙️ Workflow
- Image Processing
  - Resize and preprocess images
  - Extract features using VGG16
- Text Processing
  - Clean captions (lowercase, remove punctuation)
  - Tokenize text
  - Convert captions into sequences
- Model Training
  - Combine image features + text sequences
  - Train LSTM model with Attention
- Inference
  - Input image → feature extraction → caption generation word by word

---

## 🛠️ Requirements
```bash
Python 3.7+
TensorFlow / Keras
NumPy
OpenCV
Pillow (PIL)
NLTK
tqdm
