### COVID-19 Drug Discovery Data

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("divyansh22/drug-discovery-data")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("divyansh22/drug-discovery-data")

# Load drug discovery data
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
for csv_file in csv_files:
    df = pd.read_csv(os.path.join(path, csv_file))
    print(f"File: {csv_file}")
    print(f"Shape: {df.shape}")
    print(f"Columns: {list(df.columns)}\n")
```

**Dataset Description:**
- IC50 data of 104 chemical molecules against COVID-19 virus
- Drug efficacy and molecular properties data
- Supports computational drug discovery research
- Perfect for Module 11: Drug Discovery in AI4PH course