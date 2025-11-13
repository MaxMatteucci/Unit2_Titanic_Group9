# Unit2_Titanic_Group9

## Project Overview
This project explores predictive modeling using BigQuery ML (BQML) on the **Titanic dataset**. The objective was to build and evaluate models that estimate passenger survival probability using logistic regression, both in a simple baseline form and with additional engineered features.  
Each team member created an individual model variant, and together, we analyzed performance, interpretability, and operational trade-offs across thresholds.

---

## Business Question
Can we accurately predict whether a passenger would survive the Titanic disaster based on manifest-level features such as class, sex, age, fare, and embarkation port?

---

## Dataset
**Source:** `bigquery-public-data.ml_datasets.titanic`  
**Features used:**  
- Pclass  
- Sex  
- Age  
- Fare  
- Embarked  
- (Engineered features in later models: Family size, Fare bucket, Sex–Class interaction)

---

## Repository Structure
Unit2_Titanic_Group9/
├─ individual/
│  ├─ 
│  ├─ 
│  └─ ...
├─ team/
│  ├─ Ops_Brief.pdf
│  └─ README.md


## Tools Used
- **Google BigQuery ML (BQML)**
- **Google Colab**
- **SQL**
- **Python (for threshold and cost analysis)**

---

## Authors
**Team 9 – MGMT 467, Purdue University**  
- Max Matteucci  
- Ethan Lebon
- Ian Hedges  
- Caleb Brunton

---


## How to Run
To reproduce our results, open the Colab notebook and upload your kaggle.json API token. The notebook will automatically download the Titanic dataset from Kaggle, upload it into your BigQuery project (database-project-467, titanic_dataset.titanic), and run all SQL and Python cells with no additional configuration. After setup, simply run each cell in order to train the baseline and engineered models, evaluate thresholds, and generate the associated plots and metrics.

## Dataset Choice
We selected the Kaggle Titanic dataset so that each team member could build their own private and reproducible BigQuery table. This avoided inconsistencies between public datasets and ensured identical schema and row counts when comparing individual work.

## Assumptions
Our modeling assumes only pre-embarkation features are available, matching the real decision scenario. Logistic regression was used for interpretability, and all labels in the Kaggle dataset were treated as accurate. Threshold adjustments were tested under the assumption that missing a true survivor is more costly than predicting survival incorrectly.
