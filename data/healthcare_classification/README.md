### Healthcare Classification Dataset

- Load the dataset in matplotlib-journey.com

```python
import kagglehub
import pandas as pd

# Download the dataset
path = kagglehub.dataset_download("prasad22/healthcare-dataset")
print(f"Dataset downloaded to: {path}")
```

- Load the dataset outside (any other environment)

```python
import kagglehub
import pandas as pd
import os

# Download the dataset
path = kagglehub.dataset_download("prasad22/healthcare-dataset")

# Load the CSV file
csv_files = [f for f in os.listdir(path) if f.endswith('.csv')]
if csv_files:
    df = pd.read_csv(os.path.join(path, csv_files[0]))
    print(f"Dataset shape: {df.shape}")
    print(f"Columns: {list(df.columns)}")
    print(df.head())
```

**Dataset Description:**
- Healthcare classification dataset (< 1MB)
- Multi-category classification problem
- Dummy healthcare data with multiple target classes
- Perfect for testing different classification algorithms
- Supports Module 5: Machine Learning, algorithm comparison, model evaluation