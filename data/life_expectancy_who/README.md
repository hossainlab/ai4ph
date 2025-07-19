### Life Expectancy (WHO) Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("kumarajarshi/life-expectancy-who")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("kumarajarshi/life-expectancy-who")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- WHO Life Expectancy dataset (< 5MB)
- Statistical analysis on factors influencing life expectancy
- 193 countries from 2000-2015 with 22 health indicators
- Features include immunization, mortality, economic factors, social factors
- Supports Module 4: Data Visualization, Module 7: Public Health Modeling, Module 8: Surveillance