### Mental Health Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("bhavikjikadara/mental-health-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("bhavikjikadara/mental-health-dataset")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Mental health analysis dataset (< 3MB)
- Comprehensive dataset for analyzing mental well-being patterns
- Features include demographic factors, lifestyle indicators, mental health metrics
- Multi-category analysis of mental health conditions and risk factors
- Supports Module 4: Data Visualization, Module 5: Machine Learning, Module 7: Public Health Modeling