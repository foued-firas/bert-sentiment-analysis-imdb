# 🎬 BERT Sentiment Analysis on IMDB Reviews

An end-to-end Natural Language Processing (NLP) project that fine-tunes a BERT model for sentiment classification on the IMDB movie reviews dataset.

## 📌 Project Overview

The objective of this project is to classify movie reviews as:

- Positive (1)
- Negative (0)

Using a pretrained Transformer model (BERT) from Hugging Face and fine-tuning it with PyTorch.

---

## 🛠️ Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- Hugging Face Datasets
- Scikit-learn
- Pandas
- NumPy
- tqdm

---

## 📊 Dataset

Dataset: IMDB Movie Reviews

- 50,000 movie reviews
- Binary sentiment classification
- Balanced dataset

Example:

| Review | Label |
|----------|----------|
| "This movie was amazing!" | Positive |
| "Worst movie I've ever watched." | Negative |

---

## 🏗️ Model Architecture

```text
Movie Review
      │
      ▼
Tokenizer
      │
      ▼
BERT Base Uncased
(768 Hidden Features)
      │
      ▼
Dropout
      │
      ▼
Linear Layer (768 → 2)
      │
      ▼
Positive / Negative
```

### Architecture Components

- BERT Base Uncased
- Hidden Size: 768
- Dropout: 0.3
- Classification Head: Linear(768, 2)

---

## ⚙️ Training Configuration

```python
Batch Size = 8
Learning Rate = 2e-5
Optimizer = AdamW
Loss Function = CrossEntropyLoss
Epochs = 1
```

Training was performed on GPU using CUDA.

---

## 📈 Results

### Training Loss

```text
0.261
```

### Test Accuracy

```text
88.67%
```

The model achieved strong performance after a single epoch of fine-tuning.

---

## 🚀 Example Prediction

```python
predict_sentiment(
    "This movie was absolutely amazing. I loved every minute."
)
```

Output:

```text
Positive
```

---

```python
predict_sentiment(
    "This is the worst movie I have ever watched."
)
```

Output:

```text
Negative
```

---


---

## 📚 Concepts Practiced

This project covers:

- NLP Fundamentals
- Text Tokenization
- Attention Masks
- Transformers
- BERT Fine-Tuning
- Binary Classification
- Cross Entropy Loss
- Backpropagation
- GPU Training with CUDA
- Model Evaluation

---


---

## 👨‍💻 Author

Firas Foued

Aspiring Data Scientist / AI Engineer

Focused on Machine Learning, Deep Learning, NLP, LLMs, and Generative AI.

---

## ⭐ If you found this project useful

Consider giving the repository a star.
