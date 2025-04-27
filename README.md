# Python Project Code
[Nguyen_Capston.ipynb](https://github.com/lenguyen8888/Berkeley_ML_AI_Capstone/blob/main/Nguyen_Capstone.ipynb)

---
# Research Question
**How can Long Short-Term Memory (LSTM) networks generate meaningful and coherent poetry using the Gutenberg Poetry Corpus?**

## Expected Data Source
The **Gutenberg Poetry Corpus** will serve as the primary dataset, which will be preprocessed for LSTM model training.

## Techniques
The project will involve:
- **Data Cleaning and Tokenization** to prepare the text.
- **Training an LSTM network** using frameworks such as TensorFlow or PyTorch.

## Expected Results
A trained LSTM model capable of producing:
- Original, **coherent, and meaningful poetry**.
- Insights into the **effectiveness of LSTMs in creative text generation**.
- A **detailed report** on methodology and findings.

## Why This Question Is Important
This project bridges **artificial intelligence and creativity**, showcasing the potential of machine learning in generating artistic outputs. Understanding how LSTMs generate poetry could inspire advancements in AI applications within:
- **Literature**
- **Education**
- **Entertainment**

Without this exploration, the potential of neural networks to **complement and innovate creative processes** may remain underutilized. By addressing this question, we can reveal how AI transforms artistic expression into something **accessible, inspiring, and impactful**.

# LSTM Poetry Generation: Exploratory Data Analysis & Model Results

## Introduction
The objective of this project is to explore how **Long Short-Term Memory (LSTM) networks** can generate **meaningful and coherent poetry** using the **Gutenberg Poetry Corpus**. This module focuses on **Exploratory Data Analysis (EDA)** to clean, preprocess, and better understand the dataset before training an LSTM-based neural network. Additionally, a baseline model was trained to evaluate initial performance and serve as a comparison in future iterations.

---

## Exploratory Data Analysis (EDA)

### Data Cleaning & Preprocessing
- Removed unnecessary symbols, punctuation, and noise.
- Tokenized text into sequences.
- Created a vocabulary and embedded words for model training.

### Feature Engineering
- Converted poetry lines into numerical sequences.
- Utilized **word embeddings** for meaningful vector representation.
- Implemented **sequence padding** for uniform input length.

### Dataset Insights
- The dataset consists of **thousands of poetry lines** with varying structure.
- Processed vocabulary size: **3,189 unique tokens**.
- Structured patterns in poetry make LSTM a suitable approach for generation.

---

## Model Architecture

### Sequential Model Summary
| Layer Type               | Output Shape    | Parameters  |
|--------------------------|----------------|-------------|
| **Embedding**           | (None, 10, 100) | 318,900     |
| **Bidirectional LSTM**  | (None, 384)     | 450,048     |
| **Dense Layer**         | (None, 3189)    | 1,227,765   |

- **Total Parameters:** **1,996,713** (Trainable: **1,996,713**, Non-trainable: **0**)
- **Bidirectional LSTM** captures contextual dependencies from both directions.
- **Dense output layer** enables word prediction for poetry generation.

---

## Training Results

### Training Process (30 Epochs)
| Epoch | Accuracy  | Loss  |
|-------|----------|------|
| 1     | 2.51%    | 7.04 |
| 5     | 6.05%    | 5.20 |
| 10    | 21.30%   | 3.75 |
| 15    | 48.05%   | 2.40 |
| 20    | 68.34%   | 1.51 |
| 25    | 83.64%   | 0.82 |
| 30    | **88.83%** | **0.52** |

### Performance Analysis
- The model **exceeded the accuracy goal** of **80%**, reaching **88.83% accuracy**.
- Loss consistently declined, showing **stable learning progression**.
- The model demonstrates **strong word prediction capabilities**, making it suitable for poetry generation.

---

## Conclusion & Next Steps
- The **LSTM model successfully learns poetry patterns** and word relationships.
- Next steps include:
  - **Fine-tuning hyperparameters** for better coherence.
  - **Exploring advanced architectures** like transformers.
  - **Expanding the dataset** for richer poetic diversity.

This project highlights how **AI can enhance artistic expression** and create **innovative creative text generation methods**.

