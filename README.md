# Drug-Drug Interaction (DDI) Classification using NLP and Machine Learning

## Project Overview

Drug-Drug Interactions (DDIs) occur when one drug affects the therapeutic effect or safety of another drug. Automatically identifying these interactions from biomedical literature is an important Natural Language Processing (NLP) task that supports clinical decision-making and pharmacovigilance.

This project develops an end-to-end NLP pipeline to classify drug-drug interactions into four predefined categories using the DDIExtraction 2013 corpus. The pipeline includes XML parsing, entity masking, text preprocessing, TF-IDF feature extraction, and multiclass classification using traditional Machine Learning algorithms.

The performance of multiple classifiers is compared using standard evaluation metrics, with **Random Forest** achieving the highest classification accuracy of **93.6%**.

---

## Dataset

**Dataset:** DDIExtraction 2013 Corpus

The dataset consists of biomedical documents annotated with drug entities and their interactions.

### Interaction Classes

- **Effect** – One drug affects the pharmacological effect of another.
- **Mechanism** – One drug alters the mechanism or metabolism of another.
- **Advise** – Medical advice regarding the simultaneous use of two drugs.
- **Int** – Drug interaction exists but does not belong to the above categories.

### Dataset Statistics

| Attribute | Value |
|----------|-------:|
| Total Samples | 4,999 |
| Number of Classes | 4 |
| Data Format | XML |
| Domain | Biomedical NLP |

---

## Project Workflow

```
XML Parsing
      │
      ▼
Entity Masking
      │
      ▼
Text Cleaning
      │
      ▼
Tokenization
      │
      ▼
Lemmatization
      │
      ▼
Train-Test Split
      │
      ▼
TF-IDF Feature Extraction
      │
      ▼
Machine Learning Models
      │
      ▼
Performance Evaluation
```

---

## Data Preprocessing

The following preprocessing steps were performed before model training:

- XML parsing to extract sentences, drug entities, and interaction labels
- Entity masking using `DRUG1` and `DRUG2`
- Text cleaning
  - Lowercase conversion
  - Removal of punctuation
  - Removal of extra whitespace
- Tokenization
- Lemmatization using NLTK WordNet Lemmatizer
- Train-Test Split (80:20)
- TF-IDF vectorization

---

## Machine Learning Models

The following supervised learning algorithms were implemented and compared:

- Naive Bayes
- Decision Tree
- Logistic Regression
- Random Forest

---

## Model Performance

| Model | Accuracy |
|----------------------|----------:|
| Naive Bayes | 87.6% |
| Decision Tree | 92.5% |
| Logistic Regression | 93.2% |
| **Random Forest** | **93.6%** |

### Best Model

**Random Forest**

Reasons for superior performance:

- Better handling of high-dimensional TF-IDF features
- Reduced overfitting through ensemble learning
- Improved generalization compared to individual decision trees

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Feature Importance (Random Forest)

---

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Matplotlib
- XML Parsing (ElementTree)

---

## Repository Structure

```
Drug-Drug-Interaction-Classification/

│── notebook/
│     └── DDI_Classification.ipynb
│
│── images/
│     ├── class_distribution.png
│     ├── confusion_matrix_rf.png
│     ├── feature_importance.png
│     └── model_comparison.png
│
│── README.md
│── requirements.txt
│── .gitignore
```

---

## Results

Random Forest achieved the highest performance among all implemented models with an accuracy of **93.6%**.

The project demonstrates that traditional Machine Learning algorithms combined with effective NLP preprocessing techniques can provide strong performance for biomedical relation extraction tasks without requiring deep learning models.

---

## Future Improvements

Potential enhancements include:

- Fine-tuning BioBERT or PubMedBERT
- Incorporating biomedical word embeddings
- Hyperparameter optimization
- Handling class imbalance using SMOTE or class weighting
- Explainable AI techniques such as SHAP or LIME

---

## Key Skills Demonstrated

- Natural Language Processing (NLP)
- Biomedical Text Mining
- XML Parsing
- Entity Masking
- Text Preprocessing
- TF-IDF Vectorization
- Feature Engineering
- Multiclass Classification
- Model Evaluation
- Machine Learning with Scikit-learn

---

## Author

**Sneha Vishwakarma**

M.Sc. Applied Statistics & Informatics  
Indian Institute of Technology Bombay
