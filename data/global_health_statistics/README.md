### Global Health Statistics

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("malaiarasugraj/global-health-statistics")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("malaiarasugraj/global-health-statistics")

# Load global health statistics
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
for csv_file in csv_files:
    df = pd.read_csv(os.path.join(path, csv_file))
    print(f"File: {csv_file}")
    print(f"Shape: {df.shape}")
    print(f"Countries: {df['Country'].nunique() if 'Country' in df.columns else 'N/A'}")
    print(f"Sample data:\n{df.head(3)}\n")
```

**Dataset Description:**
- Global health statistics by country
- Disease prevalence, treatments, and health outcomes
- Mortality rates and health indicators worldwide
- Supports Module 4: Data Visualization and Module 7: Public Health Modeling