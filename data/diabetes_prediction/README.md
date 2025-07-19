### Diabetes Prediction Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("mathchi/diabetes-data-set")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("mathchi/diabetes-data-set")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- UCI Diabetes dataset (< 1MB)
- 768 instances with 8 medical attributes
- Binary classification: Diabetes onset prediction
- Features include glucose, blood pressure, BMI, age
- Supports Module 5: Machine Learning and Module 7: Public Health Modeling