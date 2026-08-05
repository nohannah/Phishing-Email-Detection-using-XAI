# Transformer-Based Phishing Email Detection with Explainable AI (XAI)

## Project Overview
Traditional rule-based phishing detection struggles with context-specific details, leading to lower accuracy. This project addresses this limitation by fine-tuning and evaluating four state-of-the-art transformer models to detect phishing emails based on contextual meaning. To ensure model transparency and trustworthiness, post hoc explainability techniques were integrated into the pipeline.

## Dataset & Methodology
* **Source Material:** A stratified random sample of 20,000 emails selected from a publicly available dataset of 82,077 labeled emails.
* **Class Preservation:** Stratified sampling ensured the original dataset's class distribution was maintained.
* **Evaluation Metrics:** Models were rigorously evaluated using Accuracy, Precision, Recall, F1-Score, and Confusion Matrices.

## Models Evaluated
* BERT 
* RoBERTa
* DistilBERT
* DeBERTa

## Key Findings
* **High Accuracy:** All four transformer models effectively captured contextual meaning, achieving approximately **99% accuracy**.
* **Top Performer:** BERT proved to be the most successful model, exhibiting the fewest misclassifications.
* **Explainability (XAI):** Post hoc analyses using **SHAP** and **LIME** provided both global and local explanations of the predictions. This transparency helps users understand how decisions are made, significantly boosting confidence in the model's reliability.
