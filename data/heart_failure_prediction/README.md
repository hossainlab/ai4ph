### Heart Failure Prediction Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("fedesoriano/heart-failure-prediction")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("fedesoriano/heart-failure-prediction")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Heart failure prediction dataset (< 1MB)
- 918 instances with 11 clinical features
- Binary classification: Heart disease prediction
- Features include chest pain type, cholesterol, ECG results, max heart rate
- Supports Module 5: Machine Learning and cardiovascular health analysis