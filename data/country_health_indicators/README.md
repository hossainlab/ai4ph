### Country Health Indicators Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("nxpnsv/country-health-indicators")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("nxpnsv/country-health-indicators")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Country-level health indicators dataset (< 2MB)
- Global health statistics by country
- Health indicators relevant to disease risk and outcomes
- Features include mortality rates, health metrics, demographic data
- Supports Module 4: Data Visualization, Module 7: Public Health Modeling, Module 8: Surveillance