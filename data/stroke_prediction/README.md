### Stroke Prediction Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("fedesoriano/stroke-prediction-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("fedesoriano/stroke-prediction-dataset")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Stroke prediction dataset (< 2MB)
- 5110 instances with 11 clinical features for predicting stroke events
- Features include age, hypertension, heart disease, glucose level, BMI, smoking status
- Binary classification: Stroke occurrence prediction
- Supports Module 5: Machine Learning, Module 7: Public Health Modeling, neurological health analysis