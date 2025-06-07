# 🛡️ Phishing Email Detection using XGBoost

A machine learning pipeline to accurately detect phishing emails based on engineered textual and structural email features. This project focuses on handling **severely imbalanced data** using techniques like **SMOTE**, **class weighting**, and **threshold tuning** to maximize **real-world performance**.

---

## 📌 Project Highlights

- ✅ Built using a dataset of **524,846 emails**, with only **~0.26% phishing emails**.
- 📊 Feature set includes email content metrics like `num_words`, `num_links`, `num_urgent_keywords`, etc.
- 🧠 Model: `XGBoostClassifier` with class imbalance tuning (`scale_pos_weight`).
- ⚖️ Handled imbalance using `SMOTE`, class weights, and threshold optimization.
- 🧪 Evaluated using `Precision`, `Recall`, `F1-Score`, and `ROC-AUC`.

---

## 🔍 Dataset Overview

| Feature                | Description                              |
|------------------------|------------------------------------------|
| `num_words`            | Total number of words in the email       |
| `num_unique_words`     | Unique word count                        |
| `num_stopwords`        | Count of common stopwords                |
| `num_links`            | Number of hyperlinks in the email        |
| `num_unique_domains`   | Number of unique domains in links        |
| `num_email_addresses`  | Number of email addresses found          |
| `num_spelling_errors`  | Count of spelling mistakes               |
| `num_urgent_keywords`  | Words like "urgent", "action", "verify"  |
| `label`                | `1 = phishing`, `0 = legitimate`         |

---

## ⚙️ Technologies Used

- Python 🐍
- Pandas, NumPy
- Scikit-learn
- Imbalanced-learn (`SMOTE`, `EasyEnsemble`)
- XGBoost
- Matplotlib, Seaborn (for EDA)

---

## 🧪 Evaluation Results

| Metric | Value |
|--------|-------|
| **Accuracy** | 96% |
| **Precision (phishing)** | 15% |
| **Recall (phishing)** | 48% |
| **F1-score (phishing)** | 0.23 |
| **ROC-AUC** | ~0.90+ |

🔁 **Threshold tuning** was used to strike a better balance between **false positives** and **false negatives**, enhancing phishing detection precision without sacrificing recall.

---

## 📈 Workflow

```text
Data Cleaning & EDA → Feature Engineering → Train/Test Split →
SMOTE Oversampling → XGBoost Model with Class Balancing →
Threshold Optimization → Evaluation & Reporting
