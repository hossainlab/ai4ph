### Maternal Health Risk Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("csafrit2/maternal-health-risk-data")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("csafrit2/maternal-health-risk-data")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Maternal health risk prediction dataset (< 1MB)
- 1014 instances with 6 features for predicting health risks in pregnant patients
- Features include age, blood pressure, blood sugar, body temperature, heart rate
- Multi-class classification: Low, Medium, High risk levels
- Supports Module 5: Machine Learning, Module 7: Public Health Modeling, maternal health analysis