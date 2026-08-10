# Contextual Semantic Analysis for Phishing Email Detection Using Transformer-Based Models with Explainable AI

## Project Authors

* Kritika Pradhanang
* Hannah No
* Shahr Bano Rezai

**Department of Computer Science**
**Asian University for Women**
**Chattogram, Bangladesh**

---

## 1. Project Overview

Phishing emails are a major cybersecurity threat because they attempt to deceive users into revealing sensitive information such as passwords, financial information, and personal credentials.

This project investigates the use of transformer-based language models for detecting phishing emails by analyzing the contextual and semantic information contained in email text.

Four transformer models were implemented and compared:

* BERT
* RoBERTa
* DistilBERT
* DeBERTa

The best-performing model was subsequently analyzed using Explainable Artificial Intelligence (XAI) techniques:

* SHAP
* LIME

The objective is not only to achieve high phishing detection performance but also to provide explanations that help users understand why an email was classified as phishing or legitimate.

---

# 2. Problem Statement

Traditional phishing email detection methods often depend on predefined rules, blacklists, and keyword-based techniques. These approaches may have difficulty detecting sophisticated phishing emails because they do not fully capture the contextual and semantic relationships within email text.

Transformer-based language models provide an opportunity to address this limitation by learning contextual relationships between words and phrases.

However, transformer models can be difficult to interpret because their predictions are not always transparent to users. Therefore, this project combines transformer-based phishing detection with Explainable AI techniques to improve the interpretability of model predictions.

---

# 3. Research Objectives

The project has the following objectives:

1. To investigate the effectiveness of transformer-based language models for phishing email detection using contextual semantic information.

2. To compare the performance of BERT, RoBERTa, DistilBERT, and DeBERTa.

3. To evaluate the models using accuracy, precision, recall, F1-score, and confusion matrices.

4. To identify the best-performing transformer model based on its classification performance and misclassification results.

5. To apply SHAP and LIME to the best-performing model to explain its predictions.

6. To investigate how Explainable AI can improve transparency and understanding of phishing email detection.

---

# 4. Research Questions

### RQ1

How effectively can transformer-based language models detect phishing emails using contextual semantic information?

### RQ2

Which transformer model (BERT, RoBERTa, DistilBERT, or DeBERTa) provides the best performance?

### RQ3

How can Explainable AI techniques help explain the predictions of the best-performing transformer model?

---

# 5. Dataset Description

The project uses a publicly available consolidated phishing email dataset containing approximately **82,077 labelled emails**.

The dataset contains two classes:

* **Phishing emails**
* **Legitimate emails**

A **stratified random sample of 20,000 emails** was selected for the experiments. Stratified sampling was used to preserve the original class distribution.

The selected dataset was divided into:

| Dataset    | Percentage |
| ---------- | ---------: |
| Training   |        70% |
| Validation |        10% |
| Testing    |        20% |

The dataset was used to train and evaluate all four transformer models under the same experimental conditions.

---

# 6. Models

The project compares four transformer-based models.

### BERT

BERT is a bidirectional transformer model that learns contextual representations by considering information from both directions surrounding a word.

### RoBERTa

RoBERTa is an optimized version of BERT with modifications to its pre-training strategy.

### DistilBERT

DistilBERT is a smaller and computationally efficient version of BERT developed using knowledge distillation.

### DeBERTa

DeBERTa introduces disentangled attention to separately represent content and positional information.

All four models were fine-tuned for phishing email classification.

---

# 7. Explainable AI

After evaluating the four transformer models, the best-performing model was selected for explainability analysis.

Two Explainable AI techniques were used:

### SHAP

SHAP was used to identify important features contributing to model predictions and to provide global and local explanations.

### LIME

LIME was used to explain individual predictions by identifying the words and textual elements that influenced a particular classification.

These techniques help users understand the reasoning behind the model's predictions.

---

# 8. Project Results

All four transformer models achieved approximately **99% accuracy**.

The number of misclassifications was:

| Model      | Misclassifications |
| ---------- | -----------------: |
| BERT       |             **39** |
| DeBERTa    |                 47 |
| DistilBERT |                 50 |
| RoBERTa    |                 58 |

BERT was selected as the best-performing model because it produced the fewest misclassifications.

SHAP and LIME analysis showed that phishing-related terms, suspicious URLs, uncommon tokens, and contextual linguistic signals contributed to the model's predictions.

---

# 9. Repository Structure

The repository is organized as follows:

```text
Hatiso_AI-Extensions/
│
├── Models/
│   ├── BERT/
│   ├── RoBERTa/
│   ├── DistilBERT/
│   └── DeBERTa/
│
├── Results/
│   ├── evaluation_results.csv
│   ├── model_comparison.csv
│   └── confusion_matrices/
│
├── Figures/
│   ├── system_architecture.png
│   ├── workflow.png
│   ├── confusion_matrix_bert.png
│   ├── confusion_matrix_roberta.png
│   ├── confusion_matrix_distilbert.png
│   ├── confusion_matrix_deberta.png
│   ├── shap_results.png
│   └── lime_results.png
│
├── Presentation/
│   └── presentation.pptx
│
├── Report/
│   └── final_report.pdf
│
├── src/
│   ├── preprocessing.py
│   ├── train.py
│   ├── evaluate.py
│   └── explainability.py
│
├── README.md
├── requirements.txt
└── .gitignore
```

> **Note:** The exact filenames inside the folders should match the files actually included in the repository.

---

# 10. Installation Requirements

## 10.1 Software Requirements

The project was developed and trained using a Google Colab environment.

The main requirements are:

* Python 3.10+
* PyTorch
* Hugging Face Transformers
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* SHAP
* LIME
* Accelerate
* SentencePiece
* Tokenizers
* Datasets

The complete Python dependencies are listed in:

```text
requirements.txt
```

---

# 11. Installation

### Step 1: Clone the Repository

Open a terminal and run:

```bash
git clone https://github.com/nohannah/Hatiso_AI-Extensions.git
```

Move into the project directory:

```bash
cd Hatiso_AI-Extensions
```

### Step 2: Create a Virtual Environment

Create a Python virtual environment:

```bash
python -m venv venv
```

### Step 3: Activate the Virtual Environment

For Windows:

```bash
venv\Scripts\activate
```

For macOS/Linux:

```bash
source venv/bin/activate
```

### Step 4: Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

---

# 12. Execution

The models were trained using Google Colab.

To reproduce the experiments:

### Step 1

Open the project notebook provided in the repository.

### Step 2

Open the notebook using Google Colab.

### Step 3

Ensure that the required dataset is available.

### Step 4

Run the preprocessing cells to clean and prepare the email dataset.

### Step 5

Create the stratified 20,000-email sample.

### Step 6

Split the data into:

```text
70% Training
10% Validation
20% Testing
```

### Step 7

Run the model training sections for:

```text
BERT
RoBERTa
DistilBERT
DeBERTa
```

### Step 8

Run the evaluation section to calculate:

```text
Accuracy
Precision
Recall
F1-score
Confusion Matrix
Misclassifications
```

### Step 9

Compare the four models and identify the best-performing model.

### Step 10

Run the SHAP and LIME explainability sections on the selected model.

### Step 11

Save the generated results and figures in the appropriate repository folders.

---

# 13. Reproducibility

To reproduce the experimental results, researchers should use the same:

* Dataset
* Stratified sampling procedure
* Training/validation/testing split
* Preprocessing procedure
* Transformer architectures
* Maximum sequence length
* Batch size
* Learning rate
* Number of training epochs
* Random seed
* Evaluation metrics

The experimental configuration used in the study includes a maximum sequence length of 256 tokens, batch size of 16, learning rate of 2 × 10⁻⁵, AdamW optimization, three training epochs, weight decay of 0.01, and random seed 42.

---

# 14. Expected Output

After executing the pipeline, the user should obtain:

1. Trained transformer models.
2. Model evaluation results.
3. Accuracy, precision, recall, and F1-score.
4. Confusion matrices.
5. Misclassification results.
6. SHAP explanations.
7. LIME explanations.
8. Comparative results between BERT, RoBERTa, DistilBERT, and DeBERTa.

The expected model comparison is approximately:

```text
BERT          → 99% accuracy → 39 misclassifications
DeBERTa       → 99% accuracy → 47 misclassifications
DistilBERT    → 99% accuracy → 50 misclassifications
RoBERTa       → 99% accuracy → 58 misclassifications
```

---

# 15. Research Contribution

This project contributes a comparative evaluation of four transformer-based models for contextual phishing email detection and integrates Explainable AI into the analysis.

The project demonstrates that transformer models can achieve high phishing detection performance while SHAP and LIME can provide additional insight into the linguistic and contextual information influencing model predictions.

---

# 16. Authors

**Kritika Pradhanang**
**Hannah No**
**Shahr Bano Rezai**

**Asian University for Women**
Department of Computer Science
