# Bangla Sentiment Analysis

**Bangla-Sentiment-Analysis** is a deep learning-based project that performs sentiment classification on Bengali product reviews, categorizing them into **Positive**, **Negative**, or **Neutral** sentiments. This was developed as part of my undergraduate thesis at BRAC University.

The system explores and compares the performance of:
- Traditional Machine Learning Models (SVM, Random Forest, etc.)
- Deep Learning Models with Word Embeddings (BiLSTM with GloVe & FastText)
- Transformer-based Models (Multilingual BERT & BanglaBERT)

---

## 🧠 Models Implemented

### ✅ Traditional ML Models
- **TF-IDF + Multinomial Naive Bayes**
- **TF-IDF + Logistic Regression**
- **TF-IDF + Random Forest**
- **TF-IDF + SVM**
- **TF-IDF + Gradient Boosting**

### ✅ Deep Learning Models
- **BiLSTM + GloVe (300d)**
- **BiLSTM + FastText (cc.bn.300.bin)**
- **BiLSTM + Fine-tuned GloVe**
- **BiLSTM + Fine-tuned FastText**

### ✅ Transformer Models
- **Multilingual BERT (bert-base-multilingual-cased)**
- **Fine-tuned Multilingual BERT**
- **BanglaBERT (csebuetnlp/banglabert)**
- **Fine-tuned BanglaBERT**

---

## 📊 Dataset

- Collected **34,800** Bengali product reviews via web scraping from [Daraz Bangladesh](https://www.daraz.com.bd/).
- Each review includes:
  - `clean_sentence`: The cleaned Bengali review text
  - `Sentiment`: Labeled as `Positive`, `Neutral`, or `Negative` based on the rating

---

## 🧪 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **Confusion Matrix**
- **Classification Report**

| Model                            | Accuracy | F1-Score |
|----------------------------------|----------|----------|
| BiLSTM + Fine-tuned FastText     | 76.47%   | 75.59%   |
| BiLSTM + Fine-tuned GloVe        | 74.94%   | 74.52%   |
| Fine-tuned Multilingual BERT     | 74.11%   | 73.10%   |
| Fine-tuned BanglaBERT            | 72.74%   | 70.57%   |
| BiLSTM + FastText (Pretrained)   | 76.47%   | 75.59%   |
| BiLSTM + GloVe (Pretrained)      | 69.58%   | 67.86%   |
| Multilingual BERT (Vanilla)      | 69.43%   | 68.97%   |
| BanglaBERT (Vanilla)             | 68.82%   | 67.27%   |


---

## ⚙️ Technologies Used

- **Python**
- **PyTorch**, **Transformers (HuggingFace)**
- **scikit-learn**
- **fasttext**
- **GloVe embeddings**
- **Matplotlib**, **Seaborn**
- **Pandas**, **NumPy**

---

## 🧾 File Structure

