# INDIVIDUAL ASSIGNMENT README 🚢📊

## Summary
This notebook recreates the full Titanic survival modeling workflow using Kaggle data and BigQuery ML. By downloading kaggle.json, loading the dataset into BigQuery, and running the provided notebook cells, anyone can reproduce the baseline and engineered models exactly.

## How to Reproduce 🔁

1. Upload your kaggle.json file in Colab:
   from google.colab import files
   files.upload()  # upload kaggle.json

2. Place it in the correct directory:
   !mkdir -p ~/.kaggle
   !cp kaggle.json ~/.kaggle/
   !chmod 600 ~/.kaggle/kaggle.json

3. Download the Titanic dataset:
   !pip install -q kaggle
   !kaggle competitions download -c titanic -p /content
   !unzip -o /content/titanic.zip -d /content

4. Load the CSV into a dataframe:
   import pandas as pd
   df = pd.read_csv("/content/train.csv")

5. Upload the data into your BigQuery project:
   from google.cloud import bigquery
   client = bigquery.Client(project="database-project-467")
   client.create_dataset("titanic_dataset", exists_ok=True)
   table_ref = "database-project-467.titanic_dataset.titanic"
   job = client.load_table_from_dataframe(df, table_ref)
   job.result()

6. Run all remaining notebook cells to reproduce every model, evaluation, and threshold analysis.

## Done 🎉
These steps fully recreate the dataset and allow the entire analysis to run identically from scratch.
