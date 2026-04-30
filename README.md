# 🤖 AI-Generated Good Text / Bad Text Analyzer

An AI-powered text analysis model that distinguishes between **malicious (bad bot)** and **benign (good bot)** AI-generated text. Built with a custom algorithm using TF-IDF vectorization and a Logistic Regression classifier, achieving a **20% accuracy improvement** over baseline approaches.

---

## 📌 Overview

This model analyzes a given piece of text against a curated set of keywords to determine whether it is AI-generated and, if so, whether it is **malicious or non-malicious**. The primary use case is **phishing email detection** — flagging AI-generated text that may be attempting to deceive or harm users.

---

## ✨ Features

- ✅ Classifies text as **Malicious** or **Non-Malicious**
- ✅ Uses **TF-IDF vectorization** for feature extraction
- ✅ Trained on labeled CSV datasets of good and bad bot text
- ✅ Outputs **accuracy score** and a detailed **classification report**
- ✅ Designed for seamless use in **Google Colab**

---

## 📂 Repository Structure

```
AI-Generated-Good-Text-Bad-Text-Analyzer/
├── AI-Generated Good Bot_ Bad Bot text analyzer.ipynb  # Main Jupyter notebook
├── Good_text.csv                                        # Dataset: benign (good bot) text samples
├── Bad_text_new.csv                                     # Dataset: malicious (bad bot) text samples
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- A Google account (for Google Colab)
- The two CSV dataset files: `Good_text.csv` and `Bad_text_new.csv`

### How to Run

1. **Open Google Colab** — [https://colab.research.google.com](https://colab.research.google.com)
2. **Upload the notebook** — `AI-Generated Good Bot_ Bad Bot text analyzer.ipynb`
3. **Run the first cell** — It will prompt you to upload files. Upload both:
   - `Good_text.csv`
   - `Bad_text_new.csv`
4. **Run the remaining cells in order** — The model will train and produce results including accuracy score and classification report.

---

## 🧠 How It Works

| Step | Description |
|------|-------------|
| 1. Data Loading | Reads good and bad bot text samples from CSV files |
| 2. Preprocessing | Cleans and prepares text data |
| 3. Feature Extraction | Applies **TF-IDF vectorization** to convert text into numerical features |
| 4. Model Training | Trains a **Logistic Regression** classifier on labeled data |
| 5. Prediction | Classifies a given input text as malicious or non-malicious |
| 6. Evaluation | Outputs accuracy score and a full classification report |

---

## 🎯 Use Case

> **Phishing Email Detection**  
> This analyzer was designed to be applied to incoming emails to detect AI-generated phishing attempts. By identifying linguistic patterns commonly used in malicious AI-generated content, it can help flag suspicious messages before they reach end users.

---

## 📊 Sample Output

```
Input: "Dear Customer, We would like to verify your account details..."
Result: Malicious
Accuracy: 1.0

              precision    recall  f1-score   support
           0       1.00      1.00      1.00         8
           1       1.00      1.00      1.00         3
    accuracy                           1.00        11
```

---

## 🛠️ Tech Stack

- **Python**
- **scikit-learn** — TF-IDF Vectorizer, Logistic Regression, classification metrics
- **pandas** — Data loading and manipulation
- **Google Colab** — Execution environment

---

## 📄 License

This project is open source. Feel free to use and build upon it.
