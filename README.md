# Multi-Format Phishing Attachment Detection

This repository contains the implementation and experimental work conducted as part of our machine learning project on malicious attachment and phishing detection.

The project is based on the **CIC-Trap4Phish** research work, which introduces a unified multi-format dataset for detecting malicious and benign samples across Word, Excel, PDF, HTML, and QR code formats.

## Project Objectives

The main objectives of this project were to:

- Reproduce the baseline machine learning experiments reported in the CIC-Trap4Phish study.
- Analyze the extracted features and investigate potential dataset quality issues.
- Develop a compact and interpretable unified feature representation across document formats.

## Methodology

For document-based formats, the experiments use static features extracted without executing the files.

The evaluated machine learning models include:

- Logistic Regression
- Random Forest
- XGBoost

The project also introduces a domain-driven feature engineering approach that maps format-specific attributes into a smaller unified representation, including:

- File size
- Text size
- Embedded objects
- Active content score
- Active content density
- External reference count
- Obfuscation score
- Structural complexity score

Additional experiments were performed to investigate data leakage risks, duplicated samples, duplicated features, and class-dependent missing-value patterns.

For QR-code phishing detection, a CNN-based image classification pipeline was implemented and evaluated using benign and malicious QR-code images.

## Experimental Workflow

1. Dataset inspection and auditing
2. Baseline model reproduction
3. Duplicate sample detection and removal
4. Analysis of missing values and suspicious class-dependent patterns 
5. Feature engineering
6. Unified feature construction
7. Model comparison
8. Analysis of experimental results


## Key Findings

- Several document datasets achieved very high classification performance using traditional machine learning models.
- Reducing the original features into a compact engineered representation preserved strong predictive performance for several file formats.
- Data auditing revealed duplicated samples and class-dependent missingness patterns that required further investigation.
- QR-code image classification was more challenging because benign and malicious QR codes can have highly similar visual structures.
- The experiments highlight the importance of evaluating both model performance and dataset quality when building security detection systems.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- TensorFlow / Keras
- Matplotlib
- Google Colab
- SHAP

## Reference

This project is based on:

**CIC-Trap4Phish: A Unified Multi-Format Dataset for Phishing and Quishing Attachment Detection**

The original study introduces the CIC-Trap4Phish dataset and its feature extraction and classification pipelines.

## Disclaimer

This repository is intended for academic and research purposes.  
Malicious files and security-related datasets should only be handled in controlled and isolated environments. 
