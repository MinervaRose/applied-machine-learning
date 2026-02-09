# Applied Machine Learning — Exoplanet Signal Classification

## Project Description

This project builds and evaluates supervised machine learning models to classify astronomical signals into exoplanet categories. The dataset is treated as a structured proxy for noisy aerospace observation signals, demonstrating how predictive models can extract reliable patterns from complex scientific measurements. The workflow emphasizes model selection, evaluation, and interpretation rather than raw accuracy optimization.

Dataset used: *Exoplanet Classification Dataset*  
https://www.kaggle.com/datasets/datatalesbyagos/exoplanet-classification-dataset

---

## What I Built

I implemented a complete applied machine learning workflow that includes:

- Data inspection and preprocessing of tabular astrophysical features  
- Stratified train/test splitting to preserve class balance  
- Feature normalization for stable model training  
- Comparison of multiple classification algorithms  
- Evaluation using accuracy, precision, recall, and F1-score  
- Confusion matrix analysis for error interpretation  
- A structured notebook that runs top-to-bottom reproducibly  

The notebook demonstrates professional model comparison and performance reasoning suitable for aerospace signal analysis and predictive analytics.

---

## Models Implemented

The project compares three classification strategies:

- **Logistic Regression** — interpretable linear baseline  
- **Random Forest** — nonlinear ensemble model  
- **Gradient Boosting** — boosted decision tree model  

This comparison highlights tradeoffs between interpretability, complexity, and generalization performance.

---

## How to Run modeling.ipynb

### Install dependencies

```bash
pip install -r requirements.txt
```

The requirements file was generated using:

```bash
pip freeze > requirements.txt
```

### Run the notebook

1. Clone or download this repository  
2. Open `modeling.ipynb` in Jupyter Notebook or Google Colab  
3. Run all cells from top to bottom  

The notebook executes without hidden state and reproduces the full modeling workflow.

Optional (Google Colab only):

If running in Colab with Google Drive storage, uncomment the setup cell at the top of the notebook.

---

## Reproducibility

This project emphasizes reproducible machine learning:

- Deterministic train/test splitting with fixed random seeds  
- Pipeline-based preprocessing to prevent data leakage  
- Explicit model configuration  
- A captured software environment via requirements.txt  
- Version-controlled workflow via Git  

Another user can recreate the environment and reproduce all results using only the repository contents.

---

## Bias Awareness

The dataset contains class imbalance, where some signal categories appear far less frequently than others. Models trained on imbalanced data may favor majority classes, reducing reliability for rare astronomical events. This imbalance introduces evaluation uncertainty and highlights the importance of fairness-aware modeling in scientific AI systems.

Future work could explore resampling techniques, class weighting, or targeted data collection to reduce bias against underrepresented signal classes.

---

## Reflection: ML Workflow Insights

Model comparison shows that nonlinear ensemble methods outperform linear baselines on complex tabular scientific data. However, higher accuracy can introduce overfitting risk, requiring careful evaluation of generalization performance. The workflow illustrates that model choice is a design decision balancing interpretability, complexity, and reliability.

This mirrors real-world applied machine learning in aerospace monitoring, where predictive systems must support expert decision-making rather than replace it.

---

## Reflection: Future Deep Learning Extensions

If extended to neural networks:

- Feature scaling would remain essential  
- Class imbalance would require specialized loss weighting  
- Additional feature engineering could improve signal separation  
- Regularization would be needed to control overfitting  

The current preprocessing pipeline provides a stable foundation for future deep learning experiments.

---

## Reflection: Autonomous Aerospace Monitoring

This project can be interpreted as a prototype component of an AI system for automated aerospace signal classification. A production system could continuously ingest new astronomical observations, evaluate classification confidence, and flag uncertain cases for expert review. The modular pipeline supports integration into larger autonomous monitoring architectures.

---

## Repository Structure

```
📂 data/
   └── ML_ready_exoplanets.csv
📓 modeling.ipynb
📄 Machine_Learning_Analysis_Report.pdf
📄 requirements.txt
📘 README.md
```

This repository demonstrates a complete, professional predictive modeling workflow suitable for applied machine learning portfolios and advanced AI system development.
