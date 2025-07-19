### Infectious Disease Prediction

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("haithemhermessi/infectious-disease-prediction")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("haithemhermessi/infectious-disease-prediction")

# Load the dataset
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(df.head())
```

**Dataset Description:**
- Data for predicting infectious disease outbreaks
- Includes epidemiological indicators and environmental factors
- Useful for machine learning models in disease surveillance
- Supports Module 7: Public Health Modeling in AI4PH course