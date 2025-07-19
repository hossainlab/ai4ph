### Disease Symptoms and Patient Profile Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("uom190346a/disease-symptoms-and-patient-profile-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("uom190346a/disease-symptoms-and-patient-profile-dataset")

# Load disease and symptoms data
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
for csv_file in csv_files:
    df = pd.read_csv(os.path.join(path, csv_file))
    print(f"File: {csv_file}")
    print(f"Shape: {df.shape}")
    print(f"Sample data:\n{df.head(3)}\n")
```

**Dataset Description:**
- Disease symptoms and patient profiles across 100+ diseases
- Relationships between patients, symptoms, and diagnoses
- Useful for clinical decision support systems
- Supports Module 5: Machine Learning and Module 7: Public Health Modeling