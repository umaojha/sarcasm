# Sarcasm Detection on Code-Mixed Hinglish Text  
### mBERT + Augmentation + Preprocessing Demonstration Notebook

This repository provides the dataset and a demonstration notebook for sarcasm detection on **code-mixed Hinglish text**.  
The notebook illustrates preprocessing, normalization techniques, and augmentation strategies that support an ongoing research study.

---

## 📂 Repository Structure

sarcasm/
│
├── rnn-mbert-sarcasm-augmentation.ipynb # Notebook showing preprocessing + augmentation
├── sarcasm_all.csv # Dataset (Hinglish + translations)
└── README.md # Documentation


## Dataset Description

This repository includes the full sarcasm dataset created by Swami et al.,
along with the complete Hindi and English translations prepared by the authors.
The dataset also contains additional preprocessing and normalization
information used in the experiments.

Below is a detailed description of each column in the dataset:

### **Columns**

| Column Name      | Description |
|------------------|-------------|
| **Unnamed: 0**   | Index column automatically generated during CSV export. Not used in the model. |
| **text**         | Original text/tweet from the Swami sarcasm dataset. This is the raw, unprocessed sample. |
| **label**        | Original label from the dataset (e.g., sarcastic vs. non-sarcastic). |
| **clean_tweet**  | Preprocessed and normalized version created by the authors. Includes text cleaning, normalization of transliterated Hinglish terms, and removal of noise. |
| **English**      | Author-generated English translation of each sample. Added to support multilingual preprocessing and cross-lingual comparison. |
| **hindi**        | Full Hindi translation created by the authors. This helps demonstrate translation quality, multilingual feature processing, and use of Hindi semantics in the study. |
| **sentiment**    | Additional sentiment annotation or polarity value assigned by the authors (if applicable for the experiment). |

### **Purpose of Including These Columns**

These columns are included for the following reasons:

- To provide full transparency of the preprocessing pipeline.
- To show the relationship between original text, cleaned text, and translated versions.
- To demonstrate how normalization, translation, and augmentation were performed.
- To help anyone reproduce or understand the logic used in the experiments.

### **Notes**

- Only the original `text` and `label` columns come from the Swami et al. dataset.  
- All other columns (`clean_tweet`, `English`, `hindi`, `sentiment`) were prepared by the authors as part of the research workflow.

---

## 🔍 What This Notebook Contains- rnn-mbert-sarcasm-augmentation

### **1. Sample Data**
A small portion of the dataset is used for demonstration.  
It includes:
- Original Hinglish text  
- Cleaned and normalized text  
- English translations  
- Hindi translations  
- Labels (sarcasm / non-sarcasm)

Only a subset is shown in the notebook to illustrate the workflow.

---

### **2. Preprocessing and Normalization**
The notebook demonstrates:

- Cleaning inconsistent Hinglish spellings  

These steps reflect the preprocessing pipeline used in the ongoing research.

---

### **3. Data Augmentation**
Two augmentation methods are shown:

#### **A. Sentence-Level**
- GPT-2 paraphrasing (`nlpaug`)
- Multilingual BERT



Each example includes original + augmented outputs.

---

### **4. Model Setup (Simplified Demo)**
The notebook includes a minimal model prototype for clarity:

- Tokenization using mBERT  
- Passing embeddings through an RNN (LSTM/BiLSTM/GRU)  
- Lightweight classifier layer  

This is a demonstration, not the full experimental setup.

---

### **5. Example Training Run (Toy Example)**


- Preprocessed text enters the model  
- Augmentation integrates into the pipeline  
- Loss evolves  
- Predictions are generated  

This avoids heavy computation while still explaining the workflow.

---

### **6. Predictions and Example Outputs**
Outputs shown include:


These demonstrate how augmentationg affects the final prediction.

---

### **7. Reproducibility Notes**
- This notebook is for explanation and transparency.  
- It illustrates the preprocessing and augmentation components described in the research work.  
  
---


## ⭐ Note

This repository accompanies an **ongoing research study**.  
Please do not cite it as a published work; instead, credit the repository if you use the code or dataset.


