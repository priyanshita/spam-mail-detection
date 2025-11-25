# Spam Mail Detection — README

## 📌 Overview
This project implements a **Spam Mail Detection System** using machine learning techniques such as **TF-IDF vectorization** and classification algorithms including:
- Multinomial Naive Bayes
- Logistic Regression
- Support Vector Machine (SVM)

It trains and evaluates models on the popular `spam.csv` dataset, performs preprocessing, feature extraction, and predicts whether a given message is **HAM (legitimate)** or **SPAM**.

---

## 📂 Project Files
- `SPAM_MAIL_DETECTION.ipynb` — Complete notebook containing all code
- `report.md` — Detailed report of the methodology and results
- `README.md` — Project overview (this file)

---

## 🧠 Features
- Loads and cleans the dataset
- Removes duplicates and unnecessary columns
- Preprocesses text (lowercasing, removing special chars, URLs, etc.)
- TF-IDF based feature extraction
- Trains three ML models
- Generates accuracy, classification reports, and confusion matrix
- Predicts label + model confidence for new custom messages

---

## 📊 Model Performance Summary
| Model | Accuracy |
|-------|----------|
| Naive Bayes | 97.10% |
| Logistic Regression | 95.65% |
| SVM (Linear) | **98.07%** |

SVM achieved the highest accuracy.

---

## 📥 Input Format
The model expects normal text messages such as:
```
"Congratulations! You've won a gift card!"
"Are we meeting today?"
```

---

## 📤 Output Format
Example:
```
Message: Hey, are we still meeting for lunch tomorrow?...
Prediction: HAM (Confidence: 99.43%)
```

---

## ▶️ How to Run
1. Upload `spam.csv` in the Colab notebook when prompted
2. Run each cell in order
3. View model performance and predictions

---

## 🛠 Tech Stack
- Python
- Scikit-learn
- Pandas & NumPy
- Google Colab

---

## 👤 Author
This README accompanies your notebook and report for the Spam Mail Detection project.

If you'd like an even more polished or professional version, feel free to ask!