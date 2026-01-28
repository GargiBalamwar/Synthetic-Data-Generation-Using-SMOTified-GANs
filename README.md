# Synthetic-Data-Generation-Using-SMOTified-GANs

## Overview
This project presents a hybrid data augmentation framework that integrates **SMOTE (Synthetic Minority Over-sampling Technique)** with **Generative Adversarial Networks (GANs)** to improve financial fraud detection.  
Fraudulent transactions are typically rare, resulting in highly imbalanced datasets that negatively impact machine learning model performance. The proposed approach generates balanced, diverse, and realistic synthetic transaction data to address this issue.

---

## Problem Statement
Financial fraud datasets suffer from severe class imbalance, causing models to:
- Favor non-fraudulent predictions
- Miss rare but critical fraud cases
- Perform poorly on recall and F1-score

This project tackles these challenges by combining structured oversampling and deep generative modeling.

---

## Proposed Approach
The framework follows a two-stage synthetic data generation pipeline:

### 1. Data Preprocessing
- Categorical features encoded using label encoding
- Numerical features normalized for model compatibility

### 2. SMOTE-Based Oversampling
- SMOTE interpolates between minority (fraud) samples
- Generates synthetic fraud records while preserving data distribution
- Reduces overfitting caused by simple duplication

### 3. GAN-Based Data Refinement
- Generator creates synthetic transaction samples
- Discriminator distinguishes real vs generated data
- Adversarial training refines samples over multiple epochs
- Captures complex, non-linear fraud patterns

---

## Workflow
1. Data preprocessing and feature engineering  
2. Class imbalance mitigation using SMOTE  
3. Synthetic data refinement using GANs  
4. Model training and evaluation  
5. Feature importance analysis  

---

## Results
- **F1-score improved from 0.82 to 0.90**
- Better balance between precision and recall
- Enhanced generalization for fraud detection models

### Key Fraud Indicators Identified
Feature importance analysis using a Random Forest classifier showed:
- Transaction amount
- Time of transaction
- Transaction frequency  
as the most influential fraud indicators.

---

## Tech Stack
- Python
- SMOTE (Imbalanced-learn)
- Generative Adversarial Networks (GANs)
- Scikit-learn
- Random Forest Classifier
- NumPy, Pandas

---

## Applications
- Financial fraud detection systems
- Banking and fintech analytics
- Cybersecurity anomaly detection
- Synthetic data generation for imbalanced datasets

---

## Future Enhancements
- Conditional GANs for class-specific generation
- Evaluation using multiple classifiers
- Integration with real-time fraud detection pipelines
- Privacy-preserving synthetic data generation

---

## Author
**Gargi Balamwar**  
B.Tech CSE Student  
