# Bangla Sentiment Analysis

**Bangla-Sentiment-Analysis** is a deep learning and traditional machine learning-based project that performs sentiment classification on Bengali product reviews, categorizing them into **Positive**, **Negative**, or **Neutral** sentiments. This was developed as part of my undergraduate thesis at BRAC University.

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

| Model                                | Accuracy | Precision | Recall | F1 Score |
|-------------------------------------|----------|-----------|--------|----------|
| **Naive Bayes (TF-IDF)**            | 65.80%   | 64.92%    | 65.80% | 64.80%   |
| **Logistic Regression (TF-IDF)**    | 68.67%   | 67.91%    | 68.67% | 67.91%   |
| **Support Vector Machine (TF-IDF)** | 68.41%   | 67.60%    | 68.41% | 67.39%   |
| **Random Forest (TF-IDF)**          | 67.56%   | 66.88%    | 67.56% | 66.78%   |
| **Gradient Boosting (TF-IDF)**      | 68.85%   | 68.41%    | 68.85% | 68.34%   |
| **BiLSTM + GloVe**                  | 69.58%   | 67.39%    | 69.58% | 67.86%   |
| **BiLSTM + FastText**               | 68.46%   | 65.39%    | 68.46% | 65.43%   |
| **Fine-tuned BiLSTM + GloVe**       | 75.99%   | 75.13%    | 75.99% | 75.38%   |
| **Fine-tuned BiLSTM + FastText**    | 77.36%   | 76.57%    | 77.36% | 76.59%   |
| **Multilingual BERT**               | 69.43%   | 68.61%    | 69.43% | 68.97%   |
| **BanglaBERT**                      | 72.72%   | 72.78%    | 72.72% | 72.69%   |
| **Fine-tuned Multilingual BERT**    | 72.44%   | 70.17%    | 72.44% | 70.17%   |
| **Fine-tuned BanglaBERT**           | 73.60%   | 72.78%    | 73.60% | 72.69%   |

---

## Technologies Used

- **Python**
- **PyTorch**, **Transformers (HuggingFace)**
- **scikit-learn**
- **fasttext**
- **GloVe embeddings**
- **Matplotlib**, **Seaborn**
- **Pandas**, **NumPy**
- **sklearn**, **imblearn**

---

## Key Contributions

- Web scraping and sentiment labeling of a large Bengali product review dataset
- Text preprocessing tailored for Bengali (e.g., normalization, stopword removal)
- Integration of domain-specific word embeddings (GloVe & FastText) fine-tuned on noisy review text
- Performance comparison across 13 models including transformers and BiLSTM variants
- Effective use of k-Fold Cross Validation and Early Stopping to mitigate overfitting

# Thesis Report

You can find the full thesis report from [Bengali sentiment analysis based on product reviews: unveiling consumer voices] (https://dspace.bracu.ac.bd/xmlui/handle/10361/25480)

## Acknowledgments

- CSE Department, BRAC University  
- Supervisor: Dewan Ziaul Karim (Lecturer, BRAC University)  
- Research inspirations from [BUET CSE NLP](https://csebuetnlp.github.io/) and [Hugging Face](https://huggingface.co/)

