# Naive Bayes Algorithm - GaussianNB

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.0%2B-orange?logo=scikit-learn)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-f37626?logo=jupyter)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

---

## Project Overview

This project demonstrates a complete implementation of the **Naive Bayes classification algorithm** using the **Gaussian Naive Bayes** classifier from scikit-learn. The project uses the classic **Iris dataset** to classify flower species into three categories based on sepal and petal measurements.

---

## Dataset

**Iris Flower Dataset** — One of the most popular datasets in machine learning for classification tasks.

| Attribute | Details |
|---|---|
| **Features** | Sepal Length, Sepal Width, Petal Length, Petal Width (in cm) |
| **Target Classes** | Setosa, Versicolor, Virginica |
| **Total Samples** | 150 (50 samples per class) |
| **Source** | [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/iris) |

---

## What's Inside This Project

This notebook walks through the following steps:

1. **Importing Required Libraries** — numpy, pandas, scikit-learn, matplotlib, seaborn
2. **Loading and Exploring the Iris Dataset** — Understanding features and target labels
3. **Creating Feature Matrix and Target Vector** — Data preparation
4. **Splitting Data** — 80/20 train-test split with fixed random state
5. **Training Gaussian Naive Bayes Model** — Model fitting on training data
6. **Making Predictions** — Predicting species on test data
7. **Model Evaluation** — Accuracy, Confusion Matrix, Classification Report (Precision, Recall, F1-Score)
8. **Cross-Validation** — 5-fold CV for model robustness
9. **Prediction Probabilities** — Confidence levels for predictions

---

## Key Results

| Metric | Value |
|---|---|
| **Test Accuracy** | 93.33% |
| **Cross-Validation Mean Accuracy** | 95.33% |
| **Cross-Validation Std Deviation** | 2.67% |

### Confusion Matrix

| | Setosa | Versicolor | Virginica |
|---|---|---|---|
| **Setosa** | 9 | 0 | 0 |
| **Versicolor** | 0 | 12 | 1 |
| **Virginica** | 0 | 1 | 7 |

---

## How Naive Bayes Works

Naive Bayes is based on **Bayes' Theorem** with the assumption of independence between features:

$$P(C_k | X) = \frac{P(X | C_k) \cdot P(C_k)}{P(X)}$$

Where:
- $P(C_k | X)$ = Posterior probability of class $C_k$ given features $X$
- $P(X | C_k)$ = Likelihood of features given class
- $P(C_k)$ = Prior probability of class
- $P(X)$ = Evidence

**GaussianNB** assumes features follow a **Gaussian (Normal) distribution** and uses the Gaussian Probability Density Function:

$$P(x_i | C_k) = \frac{1}{\sqrt{2\pi\sigma_{k,i}^2}} \exp\left(-\frac{(x_i - \mu_{k,i})^2}{2\sigma_{k,i}^2}\right)$$

---

## Technologies Used

- **Python 3.8+**
- **NumPy** — Numerical computing
- **Pandas** — Data manipulation
- **scikit-learn** — Machine learning (GaussianNB, train_test_split, metrics)
- **Matplotlib** — Visualization
- **Seaborn** — Statistical data visualization
- **Jupyter Notebook** — Interactive development

---

## Getting Started

### Prerequisites

Make sure you have Python installed. Then install the required packages:

```bash
pip install -r requirements.txt
```

### Running the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/adiratna89/Implementation-of-Naive-Bayes-Algorithm---GaussianNB.git
   ```
2. Navigate to the project folder:
   ```bash
   cd Implementation-of-Naive-Bayes-Algorithm---GaussianNB
   ```
3. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
4. Open and run the `notebooks/*.ipynb` file cell by cell.

---

## Project Structure

```
Implementation-of-Naive-Bayes-Algorithm---GaussianNB/
│
├── notebooks/Implementation of Naive Baye's Algorithm - GaussianNB.ipynb  # Main notebook
├── README.md                                                      # Project documentation
├── requirements.txt                                               # Python dependencies
└── .gitignore                                                     # Git ignore file
```

---

## Why Naive Bayes?

- Fast and efficient, even on small datasets
- Works well with high-dimensional data
- Simple to implement and interpret
- Performs well even when independence assumption is violated
- Great baseline model for classification tasks

---

## License

This project is licensed under the MIT License.

---

**Developed by Adiratna Kamble** | [adiratna89](https://github.com/adiratna89)

## DevOps & Tooling

This repository uses modern development practices and tooling:

### Continuous Integration (CI)
- **GitHub Actions** — Automated validation on every push and pull request
- Validates Python syntax, dependencies, and project structure
- Workflow: `.github/workflows/ci.yml`

### Code Quality
- **Pre-commit Hooks** — Automatic code formatting and linting before commits
- Tools: Black (formatting), isort (imports), flake8 (linting), nbQA (notebooks)
- Config: `.pre-commit-config.yaml`

### Code Ownership
- **CODEOWNERS** — Automatic reviewer assignment for pull requests
- Config: `.github/CODEOWNERS`

### Project Website
- **GitHub Pages** — Live project landing page
- Deployed automatically on push
- Config: `.github/workflows/pages.yml`

## Community & Support

### Contributing
Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests.

### Code of Conduct
This project adheres to the [Contributor Covenant Code of Conduct](CODE_OF_CONDUCT.md).

### Security
To report a security vulnerability, please see [SECURITY.md](SECURITY.md).

### Funding
If you find this project helpful, consider supporting it. See [FUNDING.yml](.github/FUNDING.yml) for available options.

## Version History

See [CHANGELOG.md](docs/CHANGELOG.md) for details.

## Citation

If you use this project in your research, please cite it using the [CITATION.cff](docs/CITATION.cff) file.
