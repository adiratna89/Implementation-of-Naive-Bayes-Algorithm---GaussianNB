# Data

This folder stores datasets used in this project.

## Datasets

### Iris Flower Dataset
The primary dataset used in this project is the **Iris Flower Dataset**, which is loaded directly from scikit-learn's built-in datasets. No external data file is required.

```python
from sklearn.datasets import load_iris
iris = load_iris()
```

## Adding New Datasets

If you want to extend this project with additional datasets (e.g., Breast Cancer, Wine, or custom datasets), place them in this folder and update the notebook accordingly.

### Supported Formats
- `.csv` — Comma-separated values
- `.xlsx` — Excel files
- `.arff` — ARFF format (common in ML)
- `.pkl` — Pickled Python objects

### Example: Loading a CSV Dataset
```python
import pandas as pd
df = pd.read_csv('data/your_dataset.csv')
```

## Dataset References

| Dataset | Source | License |
|---------|--------|--------|
| Iris Flower | [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/iris) | Public Domain |

---
*Keep this folder organized. Delete any datasets you no longer need.*
