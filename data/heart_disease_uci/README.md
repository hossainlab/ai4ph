### Heart Disease UCI Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("johnsmith88/heart-disease-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("johnsmith88/heart-disease-dataset")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Classic UCI Heart Disease dataset (< 1MB)
- 303 instances with 14 attributes
- Binary classification: Heart disease present/absent
- Perfect for Module 5: Machine Learning fundamentals
- Ideal for classification algorithms and model evaluation