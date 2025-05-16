# Python Project Code
[Nguyen_Capstone.ipynb](https://github.com/lenguyen8888/Berkeley_ML_AI_Capstone/blob/main/Nguyen_Capstone.ipynb)

---
Below is the rewritten capstone project report in Markdown:

---

# Capstone Project: Generating Shakespearean Text with NLP and LSTM  
**Final Report**

---

## 1. Define the Problem Statement

### Objective
Investigate how Long Short-Term Memory (LSTM) networks can be applied to generate meaningful, original poetry in a Shakespearean style. The goal is to understand word relationships and contextual dependencies within Shakespeare's Sonnets to produce creative, stylistically appropriate verses.

### Challenges & Benefits

- **Challenges:**
  - Curating and cleaning a dataset that reflects the rich, archaic language and structure of Shakespearean poetry.
  - Modeling sequential text data to capture the nuances of poetic language.
  - Balancing creative output with the necessity for coherent, logical structure.

- **Benefits:**
  - Merging artificial intelligence with artistic creativity.
  - Enhancing applications in literature, education, and entertainment.
  - Enabling further innovation in machine learning’s role in creative writing.

---

## 2. Model Outcomes or Predictions

### Learning Type & Expected Output
- **Learning Type:**  
  The problem is framed as a **sequence prediction task**—a classification problem where every token (word) is predicted based on preceding tokens. A **supervised learning** approach is used.

- **Expected Output:**  
  - A trained LSTM model that generates a sequence of tokens forming coherent, Shakespearean-style poetry.
  - Original verses that maintain structure and authenticity, reflecting both the language and stylistic nuances of Shakespeare’s work.

---

## 3. Data Acquisition

### Primary Data Source
- **Dataset:**  
  The Shakespearean Sonnets serve as the primary dataset because they provide the necessary historical, linguistic, and poetic context.

### Data Sourcing and Visualization
- **Multiple Sources:**  
  While Shakespearean Sonnets form the core dataset, enrichment could come from other historical texts or poetry corpora to enhance linguistic diversity.
  
- **Visualization:**  
  Visualizations such as token frequency distributions or word clouds can reveal recurring patterns, thematic clusters, and the overall richness of the vocabulary. These insights confirm the dataset’s potential for training an LSTM model.

---

## 4. Data Preprocessing/Preparation

### Data Cleaning & Tokenization
- **Cleaning Techniques:**  
  - Removal of extraneous symbols, punctuation, and noise.
  - Lowercasing and normalization to reduce vocabulary sparsity.
  
- **Tokenization:**  
  - The text is segmented into sequences of tokens representing individual words or punctuation.
  - A vocabulary is built from these tokens (our exploratory analysis revealed approximately 3,189 unique tokens).

### Dataset Splitting & Encoding
- **Splitting:**  
  - The dataset is split into training and test sets (e.g., an 80/20 split) to ensure the model is evaluated on unseen sequences.
  
- **Encoding & Padding:**  
  - Text sequences are converted into numerical representations using word embeddings.
  - Sequence padding is applied to maintain consistent input length across training batches.

---

## 5. Modeling

### Selected Approach
- **Algorithm:**  
  - An LSTM network is chosen for its capability to capture long-term sequence dependencies.
  - A **bidirectional LSTM** is also implemented to capture contextual cues from both past and future tokens.

### Model Architecture

| **Layer Type**         | **Output Shape** | **Parameters** |
|------------------------|------------------|----------------|
| Embedding              | (None, 10, 100)  | 318,900        |
| Bidirectional LSTM     | (None, 384)      | 450,048        |
| Dense (Output Layer)   | (None, 3189)     | 1,227,765      |
| **Total**              | —                | 1,996,713      |

- **Frameworks:**  
  The model is implemented using deep learning frameworks such as **TensorFlow or PyTorch**, which support complex neural network construction, training, and evaluation.

---

## 6. Model Evaluation

### Evaluation Metrics and Techniques

- **Current Evaluation:**  
  - Accuracy improved from 2.51% on Epoch 1 to 88.83% on Epoch 30.
  - Loss consistently decreased from 7.04 to 0.52, indicating a stable learning process.

- **Future Improvements:**  
  - **Additional Metrics:**  
    Integrate metrics such as **F1 Score** and **AUC (Area Under the Curve)** to better assess performance on token classification.
  
  - **Text Style Analysis:**  
    Use n-gram comparisons to evaluate stylistic consistency and coherence in the generated poetry.
    
  - **Advanced Approaches:**  
    With advances in large language models (LLMs), exploring LLM integrations and prompt-based techniques could elevate the quality and creativity of the generated poetry.

---

## Exploratory Data Analysis (EDA) & Training Results

### Introduction
This phase involved a deep dive into the dataset to facilitate effective preprocessing and form the basis for training an LSTM model. A baseline model was developed to provide initial performance metrics and guide future improvements.

### EDA: Data Cleaning & Preprocessing
- **Steps Taken:**  
  - Removed unnecessary symbols and punctuation.
  - Tokenized text into manageable sequences and built a comprehensive vocabulary.
  
- **Feature Engineering:**  
  - Converted lines of poetry into numerical sequences.
  - Applied word embeddings for richer vector representations.
  - Implemented sequence padding for uniform input dimensions.

### Dataset Insights
- The dataset consisted of thousands of poetry lines.
- Approximately 3,189 unique tokens were identified.
- The structured nature of the poetry makes LSTM an appropriate model for the task.

### Model Architecture Recap

| **Layer Type**         | **Output Shape** | **Parameters** |
|------------------------|------------------|----------------|
| Embedding              | (None, 10, 100)  | 318,900        |
| Bidirectional LSTM     | (None, 384)      | 450,048        |
| Dense (Output Layer)   | (None, 3189)     | 1,227,765      |
| **Total**              | —                | 1,996,713      |

- The **Bidirectional LSTM** enhances contextual understanding.
- The **Dense layer** maps learned representations to a probability distribution over all vocabulary tokens.

### Training Results

| **Epoch** | **Accuracy** | **Loss** |
|-----------|--------------|----------|
| 1         | 2.51%        | 7.04     |
| 5         | 6.05%        | 5.20     |
| 10        | 21.30%       | 3.75     |
| 15        | 48.05%       | 2.40     |
| 20        | 68.34%       | 1.51     |
| 25        | 83.64%       | 0.82     |
| 30        | 88.83%       | 0.52     |

The results indicate steady improvement in accuracy and a consistent decline in loss, demonstrating the model’s effective learning progression.

---

## Conclusion & Next Steps

### Summary
The project demonstrates that LSTM networks can learn the intricate patterns of Shakespearean poetry and generate coherent, stylistically authentic text. The combination of thorough exploratory data analysis, diligent preprocessing, and robust model design has proved essential.

### Next Steps
- **Hyperparameter Tuning:** Further optimize the model by fine-tuning hyperparameters.
- **Advanced Architectures:** Consider experimenting with transformer networks and exploring LLM-based approaches with prompt engineering.
- **Enhanced Evaluation:** Incorporate additional evaluation metrics such as the F1 score, AUC, and detailed text style analyses via n-gram comparisons.
- **Dataset Expansion:** Augment the dataset with other poetic sources to increase output diversity and improve the richness of the generated text.

---

This report underscores the transformative potential of artificial intelligence in creative text generation, blending classical literature with the latest advancements in machine learning, and paving the way for future innovations in this interdisciplinary field.