# Custom StandardScaler and Feature Engineering

## Project Overview

This project focuses on understanding and implementing custom Scikit-learn transformers from scratch. It demonstrates how to build stateful and stateless transformers, perform feature engineering, and combine custom transformations using `FeatureUnion`.

## Objectives

- Understand the difference between stateful and stateless transformers.
- Implement a custom StandardScaler-like transformer.
- Apply inverse transformations to recover original data.
- Extend the custom standardizer with a shrink factor.
- Build a stateless custom transformer for feature engineering.
- Combine multiple custom transformers using `FeatureUnion`.

## Implementation

### 1. Custom Standardizer

Implemented a custom transformer that calculates the mean and standard deviation from training data and applies standardization to both training and test datasets.

### 2. Inverse Transformation

Implemented `inverse_transform()` to recover the original values from standardized data.

### 3. Shrink Factor

Extended the custom standardizer with a configurable `shrink_factor` parameter to control the scale of transformed features.

### 4. Feature Averager

Created a stateless custom transformer that calculates the row-wise mean and divides it by the row-wise maximum.

### 5. Feature Union

Combined the custom standardizer and feature averager using Scikit-learn's `FeatureUnion` to generate a unified feature set.

## Technologies

- Python
- NumPy
- Pandas
- Scikit-learn
- Pytest
- Jupyter Notebook

## Testing

Each implementation step was validated using the provided automated tests.

All five test stages passed successfully:

- Custom Standardizer
- Inverse Transformation
- New Standardizer with Shrink Factor
- Feature Averager
- Feature Union with Custom Transformers

## Repository Structure

```text
.
├── 05-Hand-Made-Standardizer.ipynb
├── tests/
│   ├── test_standardizer.py
│   ├── test_new_standardizer.py
│   ├── test_feature_averager.py
│   └── test_feature_union_custom_transformers.py
└── README.md
```

## Key Learnings

This project provided practical experience in building custom Scikit-learn transformers, implementing the `fit()`, `transform()`, and `inverse_transform()` methods, and creating reusable preprocessing pipelines.

---

*Part of my Data Science and Machine Learning learning portfolio.*
