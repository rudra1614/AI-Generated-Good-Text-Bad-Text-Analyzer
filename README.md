# 🤖 AI-Generated Good Text / Bad Text Analyzer

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python&logoColor=white)
![Platform](https://img.shields.io/badge/Platform-Google%20Colab-orange?logo=googlecolab&logoColor=white)
![ML](https://img.shields.io/badge/ML-Scikit--Learn-green?logo=scikit-learn&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-TF--IDF-purple)
![License](https://img.shields.io/badge/License-MIT-lightgrey)

> An AI-powered text classification model that distinguishes between **malicious (bad)** and **benign (good)** AI-generated text — originally designed to detect phishing emails.

---

## 📌 Overview

This project builds a machine learning pipeline that:

- Reads labeled **Good Text** and **Bad Text** from CSV datasets
- Extracts features using **TF-IDF vectorization**
- Trains a classifier to identify whether a given text sample is malicious or benign
- Achieves a **20% accuracy improvement** over baseline through custom algorithm development

The primary use case is **email phishing detection** — identifying AI-generated phishing attempts by analyzing suspicious patterns in text.

---

## ✨ Features

- 📂 Upload your own Good/Bad text CSV datasets directly in Google Colab
- 🔍 TF-IDF-based keyword and phrase analysis
- 🏷️ Binary classification: **Malicious** vs. **Non-malicious**
- 📊 Outputs accuracy score and a full classification report (precision, recall, F1-score)
- 📈 Visual output (confusion matrix / feature importance plot)

---

## 🗂️ Repository Structure

```
AI-Generated-Good-Text-Bad-Text-Analyzer/
├── AI-Generated Good Bot_ Bad Bot text analyzer.ipynb   # Main Jupyter/Colab notebook
├── Good_text.csv                                         # Labeled benign text samples
├── Bad_text_new.csv                                      # Labeled malicious text samples
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites

- A **Google account** (for Google Colab)
- The two dataset files included in this repository:
  - `Good_text.csv`
  - `Bad_text_new.csv`

### Running the Notebook

1. Open [Google Colab](https://colab.research.google.com/) and upload (or open from GitHub) the notebook:
   `AI-Generated Good Bot_ Bad Bot text analyzer.ipynb`

2. **Run the first cell** — it will prompt you to upload files. Upload both:
   - `Good_text.csv`
   - `Bad_text_new.csv`

3. **Run the remaining cells sequentially** (top to bottom). Each section handles a distinct part of the pipeline:
   | Step | Description |
   |------|-------------|
   | 1 | File upload & data loading |
   | 2 | Data preprocessing & TF-IDF vectorization |
   | 3 | Model training & evaluation |
   | 4 | Prediction on custom input text |
   | 5 | Visualization of results |

4. To test a custom phrase, locate the prediction cell and replace the sample input text with your own.

---

## 📊 Model Performance

| Metric    | Score |
|-----------|-------|
| Accuracy  | 100% (on test split) |
| Precision | 1.00  |
| Recall    | 1.00  |
| F1-Score  | 1.00  |

> **Note:** Results above reflect the provided sample dataset. Performance may vary on larger, more diverse datasets.

---

## 🧠 How It Works

```
Raw Text Input
      │
      ▼
TF-IDF Vectorization
(converts text to numerical feature vectors)
      │
      ▼
Machine Learning Classifier
(trained on Good/Bad labeled data)
      │
      ▼
Prediction: Malicious ❌  or  Non-Malicious ✅
```

1. **Data Loading** — Both CSV files are read and combined with binary labels (`0` = Good, `1` = Bad).
2. **Feature Extraction** — TF-IDF transforms text into weighted term-frequency vectors.
3. **Training** — A classifier is trained on the vectorized data.
4. **Evaluation** — Accuracy, precision, recall, and F1-score are reported.
5. **Prediction** — Any new text can be passed through the trained model for classification.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Google Colab | Development & execution environment |
| Pandas | Data loading and manipulation |
| Scikit-learn | TF-IDF vectorization & classification |
| Matplotlib | Result visualization |

---

## 💡 Use Cases

- **Phishing email detection** — Flag AI-generated phishing attempts before they reach users
- **Content moderation** — Identify harmful or manipulative AI-generated content
- **Spam filtering** — Extend to classify spam vs. legitimate messages

---

## 🔮 Future Improvements

- [ ] Expand datasets with more diverse good/bad text examples
- [ ] Experiment with deep learning models (BERT, GPT-based classifiers)
- [ ] Add a web interface for real-time text analysis
- [ ] Support multi-class classification (e.g., phishing, spam, safe, promotional)
- [ ] Integrate with email clients via an API

---

## 👤 Author

**Rudra Naik**
- GitHub: [@rudra1614](https://github.com/rudra1614)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

