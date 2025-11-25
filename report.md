# 📄 Spam Mail Detection Report

## **1. Introduction**
This project focuses on building a **Spam Mail Detection System** using machine learning models. The dataset used is the widely known **spam.csv**, which contains labeled email/text messages categorized as *ham* (legitimate) or *spam*.

The goal is to:
- Clean and preprocess the data
- Convert text into numerical features using **TF-IDF**
- Train multiple ML models
- Evaluate their performance
- Test the model with sample messages

---

## **2. Dataset Overview**
- **Initial Shape:** (5572, 5)
- Dataset contained unnecessary columns which were removed.
- Only two columns retained:
  - `label` – ham/spam
  - `message` – text content

After cleaning duplicates:
- **Final Shape:** (5169, 2)

### **Class Distribution**
- **Ham:** 4516
- **Spam:** 653

The data is imbalanced, but still usable for classification.

---

## **3. Data Preprocessing**
### Steps performed:
1. Lowercasing text
2. Removing URLs
3. Removing digits and special characters
4. Removing extra spaces
5. Label encoding (ham = 0, spam = 1)

A new column `cleaned_message` was created using the preprocessing function.

---

## **4. Train-Test Split**
- 80% Training (4135 samples)
- 20% Testing (1034 samples)

TF-IDF vectorization was used with:
- `max_features=3000`
- `min_df=2`
- `max_df=0.8`
- English stopwords removed

Feature matrix shape:
- **(4135, 2749)**

---

## **5. Model Training & Evaluation**
Three ML models were trained:

### ✅ **1. Multinomial Naive Bayes**
- **Accuracy:** 0.9710
- Excellent recall for ham; moderate recall for spam.

### ✅ **2. Logistic Regression**
- **Accuracy:** 0.9565
- High precision but lower recall for spam.

### 🌟 **3. Support Vector Machine (SVM)** *(Best Model)*
- **Accuracy:** 0.9807
- Highest overall performance
- Best spam detection capability

---

## **6. Confusion Matrix (Naive Bayes)**
```
[[902   1]
 [ 29 102]]
```
- **TN:** 902
- **FP:** 1
- **FN:** 29
- **TP:** 102

Shows the dataset is slightly imbalanced and NB misclassifies some spam.

---

## **7. Testing With Sample Messages**
Below are predictions using the Naive Bayes model:

| Message (Shortened) | Prediction | Confidence |
|---------------------|------------|------------|
| Congratulations... | SPAM | 92.09% |
| Hey, are we still meeting... | HAM | 99.43% |
| URGENT: Your account... | SPAM | 79.06% |
| Can you send me the project... | HAM | 92.33% |

---

## **8. Conclusion**
The **Spam Mail Detection System** performs extremely well, with the **SVM model achieving the best accuracy (98%)**. The dataset preprocessing and TF-IDF vectorization contributed strongly to model effectiveness.

The system can confidently classify most spam messages and can be extended for production use, such as:
- Email filtering
- SMS fraud detection
- Automated classification apps

---

## **End of Report**
This markdown report summarizes the full workflow, dataset, models, evaluations, and test results of the project.