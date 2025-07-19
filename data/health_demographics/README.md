### Health and Demographics Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("uom190346a/health-and-demographics-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("uom190346a/health-and-demographics-dataset")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Health and demographics analysis dataset (< 5MB)
- Life expectancy analysis with demographic correlations
- Features include population characteristics, health outcomes, socioeconomic factors
- Multi-dimensional analysis of health determinants
- Supports Module 4: Data Visualization, Module 5: Machine Learning, Module 7: Public Health Modeling