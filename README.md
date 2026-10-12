# King County House Price Analysis

A notebook-based machine-learning project that explores King County house
sales, groups sale prices into categories, and compares classification models.

## Dataset

The supplied dataset is `data/raw/kc_house_data.csv`. It contains King County
house-sale records; the original download source is not specified in this
repository.

## Approach

- Explore and clean the sale records, then engineer property and location
  features.
- Create a categorical `price_class` target and split the data into training,
  validation, and test sets.
- Scale features and compare Logistic Regression, K-Nearest Neighbors, Random
  Forest, and Neural Network classifiers.
- Use K-Means in feature engineering and in a separate clustering analysis.
- Review model comparisons in `notebooks/final_comparison.ipynb`.

This repository focuses on classifying price ranges; it does not document a
continuous-price regression result.

## Run

Python 3.11 is recommended. From the repository root:

```bash
python -m venv .venv
```

Activate the environment, then install dependencies and start JupyterLab:

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
jupyter lab
```

Run the notebooks in order:

1. `notebooks/data_processing/01_data_exploration.ipynb`
2. `notebooks/data_processing/02_data_cleaning.ipynb`
3. `notebooks/data_processing/03_feature_engineering.ipynb`
4. `notebooks/data_processing/04_scaling_train_val_test_split.ipynb`
5. The notebooks under `notebooks/models/`
6. `notebooks/final_comparison.ipynb`

## Results

The final comparison notebook reports the model comparisons and conclusions.
Results depend on running the notebooks in the sequence above.
