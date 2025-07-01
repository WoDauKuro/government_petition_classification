# 📝 Government Petitions NLP Classification Project

This repository contains the implementation and report for a Natural Language Processing (NLP) project focused on analyzing and classifying government petitions. The work showcases advanced techniques in supervised and semi-supervised learning using the **DistilBERT** transformer model and a **RandomForest** classifier.

## 🔍 Project Overview

The project was divided into two main tasks:

### 📌 Task 1 – Topic Classification
A multi-class classification task to categorize petitions into predefined topics using text and structured metadata.

- ✅ Model Used: DistilBERT + Dense Layers
- ✅ Accuracy: **99%** (exceeding the 86% benchmark)
- ✅ 7-class classification with ≤13% misclassification rate per class
- ✅ No overfitting observed (validated via stratified 5-fold cross-validation)

### 📌 Task 2 – Petition Importance Classification
A binary classification task to predict whether a petition is “important” or “not important.”

- ✅ Models Used: DistilBERT-based Neural Network and RandomForest (baseline)
- ✅ Accuracy: **89.74%** (DistilBERT) vs. 97.43% (RandomForest)
- ✅ Semi-supervised learning employed to address the high number of unlabeled observations
- ✅ Addressed ethical issues including bias, transparency, and fairness

## 📁 Repository Contents

| File | Description |
|------|-------------|
| `task1_topic_classification.ipynb` | Jupyter notebook containing code for Task 1 using DistilBERT |
| `task2_petition_importance.ipynb` | Jupyter notebook containing code for Task 2 with both DistilBERT and RandomForest models |
| `report.pdf` | Full project report including data exploration, modeling, ethical considerations, and evaluation |

## ⚠️ Data Disclaimer

Due to data privacy concerns and ethical considerations, **the dataset used in this project will not be shared publicly**. However, the notebooks have been structured so that others can adapt the code to similar datasets.

## ⚖️ Ethical Considerations

This project incorporated an **ethical audit** using the **Data Hazards Framework**, identifying key risks related to fairness, transparency, and democratic engagement:

### 🧠 Identified Hazards:

- **Bias Amplification**: Historical inequalities in petition engagement could cause the model to deprioritize important issues raised by marginalized communities.
- **Automation Surprise**: Over-reliance on the model might result in critical petitions being overlooked without adequate human oversight.
- **Incompleteness**: Representation gaps—especially petitions from rural areas or non-mainstream issues—might skew model behavior and reinforce exclusion.

### ✅ Mitigation Strategies:

- Conduct regular **bias audits** and performance checks across demographic subgroups.
- Implement **human-in-the-loop systems** for contentious or borderline cases.
- Continuously **monitor ethical performance**, especially on high-stakes predictions.

> 🔍 The goal was to develop not just a performant model, but a **responsible** one — ensuring that algorithmic decisions support inclusive and equitable democratic processes.

---

## 🧠 Key Concepts and Tools

- **Models**: DistilBERT, RandomForest
- **Techniques**: Semi-supervised learning, TF-IDF, pseudo-labeling, entity handling
- **Libraries**: Hugging Face Transformers, Scikit-learn, NLTK, Pandas, NumPy
- **Other**: Stratified K-Fold, Gradient Clipping, Feature Engineering, Class Weighting