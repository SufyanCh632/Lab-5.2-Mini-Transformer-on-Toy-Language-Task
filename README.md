# Lab 5.2 — Mini-Transformer on Toy Language Task

## 📌 Project Overview

This project implements a Mini-Transformer model using PyTorch to perform binary classification on a randomly generated toy dataset.

The model uses an Embedding Layer, Transformer Encoder, Mean Pooling, and a Fully Connected Layer to classify sequences into two categories based on whether the sum of their elements is even or odd.

## 🎯 Objectives

- Generate a toy dataset containing integer sequences.
- Create binary labels using even/odd sum classification.
- Convert integer tokens into embedding vectors.
- Implement a Transformer Encoder using PyTorch.
- Train the model using the Adam optimizer.
- Evaluate model performance using test accuracy.

## 🛠️ Technologies Used

- Python
- PyTorch
- Deep Learning
- Transformer Encoder
- Neural Networks

## 📂 Project Structure

```text
Lab-5.2-Mini-Transformer/
│
├── mini_transformer.py
├── README.md
└── requirements.txt
```

## 📊 Dataset Description

A randomly generated dataset is used for this experiment.

| Parameter | Value |
|---|---:|
| Total samples | 200 |
| Sequence length | 10 |
| Vocabulary size | 20 |
| Training samples | 150 |
| Testing samples | 50 |
| Number of classes | 2 |

### Label Generation

Labels are generated based on the sum of each sequence:

- **Class 0:** Even sum.
- **Class 1:** Odd sum.

```python
data = torch.randint(0, 20, (200, 10))
labels = (data.sum(1) % 2).long()
```

## 🧠 Model Architecture

The TinyTransformer model consists of:

1. **Embedding Layer:** Converts token IDs into 32-dimensional vectors.
2. **Transformer Encoder:** Processes input sequences using self-attention.
3. **Mean Pooling:** Combines sequence representations.
4. **Fully Connected Layer:** Produces two classification scores.

### Model Configuration

| Parameter | Value |
|---|---:|
| Vocabulary size | 20 |
| Embedding dimension | 32 |
| Attention heads | 4 |
| Transformer layers | 2 |
| Output classes | 2 |
| Learning rate | 0.001 |
| Training epochs | 10 |
| Optimizer | Adam |
| Loss function | Cross Entropy |

## ⚙️ Training Process

The model is trained for 10 epochs using:

- Forward propagation
- Cross-entropy loss calculation
- Backpropagation
- Adam optimizer updates

## 📈 Evaluation

The trained model is evaluated using the 50 test samples.

Evaluation includes:
- Actual labels
- Predicted labels
- Test accuracy

Accuracy is calculated as:

```python
acc = (predictions == test_y).float().mean()
```

## 🚀 Installation and Execution

### 1. Install Python Dependencies

```bash
pip install torch
```

### 2. Run the Project

```bash
python mini_transformer.py
```

## 📌 Expected Results

The program displays:

- Dataset and label shapes.
- First five generated sequences.
- Model architecture.
- Training loss for each epoch.
- Actual and predicted test labels.
- Final test accuracy.

*Note: Results may vary because the dataset and model parameters are randomly initialized.*

## 📚 Learning Outcomes

Through this lab, I learned:

- How Transformer Encoder layers work.
- How token embeddings are implemented.
- How self-attention processes sequence data.
- How to train a Transformer model using PyTorch.
- How to evaluate a binary classification model.

## 👨‍💻 Author

**Muhammad Suffiyan Rafi**

Computer Science Graduate | Python | AI/ML | Deep Learning

---

**Project:** Lab 5.2 — Mini-Transformer on Toy Language Task  
**Category:** Deep Learning / Natural Language Processing  
**Framework:** PyTorch
