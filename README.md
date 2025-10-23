# TBM_rock-mass-classification_tunnelling-himalayas_ML  
### Machine Learning Approach for Rock Mass Classification with Imbalanced Database of TBM Tunnelling in Himalayan Geology  

**Authors:** Tek Bahadur Katuwal, Krishna Kanta Panthi, Chhatra Bahadur Basnet  
**Published in:** *Rock Mechanics and Rock Engineering (2024)*  
**DOI:** [https://doi.org/10.1007/s00603-024-04212-x](https://doi.org/10.1007/s00603-024-04212-x)

---

## 📚 Table of Contents
1. [Overview](#1-overview)
2. [Publication Citation](#2-publication-citation)
3. [Key Objectives](#3-key-objectives)
4. [Database Availability](#4-database-availability)
5. [Repository Structure](#5-repository-structure)
6. [Methodology](#6-methodology)
7. [Findings](#7-findings)
8. [Contributions](#8-contributions)
9. [Conclusion](#9-conclusion)
10. [Reference](#-reference)
11. [Keywords](#-keywords)


---

## 1. Overview
This repository presents a **machine learning (ML)-based framework** for classifying rock mass quality classes in tunnel boring machine (TBM) tunnelling projects, specifically in the **complex geological setting of the Himalayas**.  
The study utilizes TBM operational data from the **Bheri Babai Diversion Multipurpose (BBDM)** project in Nepal and addresses the challenge of **imbalanced datasets** in rock mass classification.  

### Key Highlights:
(a) Consideration of complex geological environments  
(b) Optimized pipelines to train ML models  
(c) Optimized pipeline for stacking ensemble learning  
(d) Imbalance handling using SMOTE  
(e) Independence from any single classifier  

---

## 2. Publication Citation
> **Katuwal, T.B., Panthi, K.K. & Basnet, C.B. (2025)**  
> *Machine Learning Approach for Rock Mass Classification with Imbalanced Database of TBM Tunnelling in Himalayan Geology.*  
> *Rock Mechanics and Rock Engineering*, 58, 11293–11318.  
> DOI: [10.1007/s00603-024-04212-x](https://doi.org/10.1007/s00603-024-04212-x)

---

## 3. Key Objectives
- Develop a **well-structured rock mass classification framework** capable of handling **imbalanced TBM tunnelling data** in complex Himalayan geology.  
- Demonstrate the **effectiveness of ensemble learning and SMOTE** in improving prediction performance for rock mass classification.

---

## 4. Database Availability
Due to project confidentiality, the dataset cannot be publicly shared.  

**Details:**
- **Source:** Bheri Babai Diversion Multipurpose (BBDM) Project, Nepal  
- **Size:** 6,879 TBM cycle datasets  
- **Features:** TBM operational parameters and corresponding RMR values  
- **Note:** Dataset is *imbalanced*, with underrepresentation of poor-quality (low RMR) rock classes  

---

## 5. Repository Structure

```
TBM_rock-mass-classification_ml-himalayas/
│
├── Data analysis and visualization/
│   ├── Data Analysis and Visualisation.ipynb 
│   │     (Script that produces plots and visualizations of Pearson Correlation Analysis, 
│   │      Visualisation with Box–Whisker and Violin Plot, Distribution with histograms, 
│   │      and Rock Mass Quality Class Visualisation)
│   ├── Performance Comparison_SMOTE.ipynb 
│   │     (Compares training and testing accuracies of eight selected classifiers)
│   └── *.jpg  
│         (Plots and visual results)
│
├── Hyperparameter optimization/
│   └── Scripts for tuning optimal hyperparameters for selected classifiers
│
├── Rock Mass Classification_SMOTE_Final/
│   └── Scripts for classifiers trained with SMOTE technique
│
├── Rock Mass Classification_without SMOTE/
│   └── Scripts for classifiers trained without SMOTE
│
└── README.md
```

---

## 6. Methodology

### Data Collection
- **6,879 TBM cycles** from a 12 km tunnel  
- Rock Mass Classification based on the **Rock Mass Rating (RMR)** system  

### ML Models Used
- **Individual Classifiers:**  
  Logistic Regression (LR), Support Vector Machine (SVM), Decision Tree (DT), Random Forest (RF), K-Nearest Neighbor (KNN), Extreme Gradient Boosting (XGBoost), and Bagging  

- **Stacking Ensemble Classifier:**  
  - Base learners: all individual classifiers  
  - **Meta-classifier:** SVM  

### Oversampling Technique
- **SMOTE (Synthetic Minority Over-sampling Technique)** applied to balance class distribution  

---

## 7. Findings

| Model | Condition | Accuracy | Precision | Recall | F1-score | PR-AUC |
|:------|:-----------|:----------|:-----------|:---------|:-----------|:---------|
| **Stacking Ensemble** | Without SMOTE | **91%** | 1 | 0.39 | 0.56 | – |
| **Random Forest** | With SMOTE | **92%** | 0.49 | 0.97 | 0.65 | 0.91 |

**Additional Insights:**
- SMOTE significantly improved prediction performance for minority classes.  
- Precision–Recall (PR) curves proved more effective than ROC curves for imbalanced classification.  

---

## 8. Contributions
- Introduced a **robust ML framework** that:  
  - Handles **imbalanced data** effectively  
  - Incorporates **complex geological factors**  
  - Employs **optimized hyperparameters** and model selection  
- Demonstrated that **including outliers** (e.g., poor rock conditions) improves model robustness.  
- Provided a **generalizable methodology** for TBM tunnelling projects in Himalayan geology.  

---

## 9. Conclusion
This study recommends using **Random Forest with SMOTE** for rock mass classification in TBM tunnelling under **complex and imbalanced geological conditions**.  
The developed framework offers a **data-driven, scalable solution** to enhance tunnelling performance, safety, and efficiency in challenging Himalayan terrains.

---

### 📘 Reference
If you use or refer to this work, please cite the following publication:  
> Katuwal, T.B., Panthi, K.K. & Basnet, C.B. (2025).  
> *Machine Learning Approach for Rock Mass Classification with Imbalanced Database of TBM Tunnelling in Himalayan Geology.*  
> *Rock Mechanics and Rock Engineering*, 58, 11293–11318.  
> DOI: [10.1007/s00603-024-04212-x](https://doi.org/10.1007/s00603-024-04212-x)

---

### 🧠 Keywords
`Machine Learning` · `Rock Mass Classification` · `TBM Tunnelling` · `Imbalanced Dataset` · `SMOTE` · `Random Forest` · `Himalayan Geology`

