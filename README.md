# Multimodal Fake News Detection Using Deep Learning 📰🧠

A deep learning-based approach for detecting fake news by combining textual and visual information to improve classification performance.

## 📌 Project Overview

Fake news spreads rapidly across digital platforms, often using misleading text and images to influence readers. This project explores deep learning architectures for fake news detection using both textual and visual features.

Multiple models are implemented and evaluated, followed by a multimodal fusion approach that integrates contextual text representations, sentiment information, similarity scores, and image features for improved classification.

## 📂 Dataset

**[Mirage-News Dataset](https://huggingface.co/datasets/anson-huang/mirage-news)**

- Contains approximately 15,000 real and fake news samples.
- Includes textual content and corresponding news images.
- Provides labels for binary classification (Real/Fake).

## 🧠 Models Implemented

The following architectures were implemented and evaluated:

- **CNN (Text-Only):** Extracts textual features for fake news classification.
- **CNN (Text + Image):** Combines textual and visual information.
- **BiLSTM (Text-Only):** Captures sequential and contextual dependencies in text.
- **BERT (Text-Only):** Uses contextual language representations for text classification.
- **BERT + CNN (Text + Image):** Integrates BERT-based text representations with CNN-based visual features.
- **Multimodal Fusion Model:** Combines BERT embeddings, sentiment vectors, cosine similarity, and visual features extracted using ResNet50, VGG16, and VGG19.

## 🚀 Proposed Multimodal Approach

The proposed approach integrates multiple feature representations:

1. **Textual Features:** Contextual representations extracted using BERT.
2. **Sentiment Features:** Sentiment vectors capturing the emotional characteristics of news content.
3. **Similarity Features:** Cosine similarity-based features.
4. **Visual Features:** Image representations extracted using pretrained ResNet50, VGG16, and VGG19 architectures.
5. **Feature Fusion:** Combines the extracted representations for final fake news classification.

## 📊 Model Performance

| Model | Accuracy | F1-Score |
|---|---:|---:|
| BERT (Text-Only) | 87% | — |
| Proposed Multimodal Fusion | **88.5%** | **0.89** |

The multimodal fusion approach achieved an accuracy of **88.5%** and an F1-score of **0.89** on the evaluated dataset.

## ⚙️ Training and Optimization

The following techniques were used to improve model training and generalization:

- Stratified data splitting
- Early stopping
- Batch normalization
- Dropout regularization
- Adam optimizer
- Multimodal feature fusion

## 🛠️ Tech Stack

- **Programming Language:** Python
- **Deep Learning:** PyTorch
- **NLP:** Hugging Face Transformers, BERT
- **Computer Vision:** TorchVision, CNN, ResNet50, VGG16, VGG19
- **Machine Learning:** Scikit-learn
- **Data Processing:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn

## 📈 Evaluation Metrics

The models were evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## 🔐 Secrets Management

Hugging Face API credentials are managed using environment variables through a `.env` file, which is excluded from version control.

Create a `.env` file in the project root if authentication is required:

```env
HF_TOKEN=your_huggingface_token_here
```

Never commit API tokens or other sensitive credentials to the repository.

## 🎓 Academic Project

**Under the guidance of:** Prof. Lakshmanan Kailasam

**Project Domain:** Deep Learning, Natural Language Processing, and Computer Vision

**Dataset:** Mirage-News (Approximately 15K samples)
