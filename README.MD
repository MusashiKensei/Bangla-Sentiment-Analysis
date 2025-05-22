# Bangla Sentiment Analysis

**Bangla-Sentiment-Analysis** is a deep learning-based project that performs sentiment classification on Bengali product reviews, categorizing them into **Positive**, **Negative**, or **Neutral** sentiments. This was developed as part of my undergraduate thesis at BRAC University.

The system explores and compares the performance of:
- Traditional Machine Learning Models 
- Deep Learning Models with Word Embeddings 
- Transformer-based Models 

---

## Models Implemented

### Traditional Machine Learning Models:
- Multinomial Naive Bayes (MNB)
- Logistic Regression (LR)
- Support Vector Machine (SVM)
- Random Forest (RF)
- Gradient Boosting Classifier (GBC)
- Vectorization: **TF-IDF**

### Deep Learning Models
- BiLSTM with pre-trained GloVe (300d)
- BiLSTM with pre-trained FastText (cc.bn.300.bin)
- Fine-tuned BiLSTM with domain-specific GloVe
- Fine-tuned BiLSTM with domain-specific FastText
- Multilingual BERT (bert-base-multilingual-cased)
- Fine-tuned Multilingual BERT
- BanglaBERT (csebuetnlp/banglabert)
- Fine-tuned BanglaBERT

---

## Dataset

- Collected **34,800** Bengali product reviews via web scraping from [Daraz Bangladesh](https://www.daraz.com.bd/).
- Each review includes:
  - `clean_sentence`: The cleaned Bengali review text
  - `Sentiment`: Labeled as `Positive`, `Neutral`, or `Negative` based on the rating

### Label Distribution:
- Positive: 45.54%
- Neutral: 20.60%
- Negative: 33.86%

---

## Evaluation Metrics

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

## Technologies Used

- **Python**
- **PyTorch**, **Transformers (HuggingFace)**
- **scikit-learn**
- **fasttext**
- **GloVe embeddings**
- **Matplotlib**, **Seaborn**
- **Pandas**, **NumPy**

---

## Highlights

- Applied 8-fold cross-validation on BiLSTM models.

- Performed domain-specific fine-tuning on GloVe and FastText embeddings.

- Utilized transformer-based models to handle linguistic complexities and spelling variations in Bengali.

- Included early stopping to avoid overfitting during training.

# Thesis Report

You can find the full thesis report from [Bengali sentiment analysis based on product reviews: unveiling consumer voices](https://dspace.bracu.ac.bd/xmlui/handle/10361/25480)


