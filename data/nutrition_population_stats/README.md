### Health Nutrition and Population Statistics

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("theworldbank/health-nutrition-and-population-statistics")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("theworldbank/health-nutrition-and-population-statistics")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- World Bank Health, Nutrition and Population Statistics (< 15MB)
- Global health data covering state of human health across countries
- Time series data on nutrition indicators, population health metrics
- Features include malnutrition rates, health expenditure, demographic indicators
- Supports Module 4: Data Visualization, Module 7: Public Health Modeling, Module 8: Surveillance