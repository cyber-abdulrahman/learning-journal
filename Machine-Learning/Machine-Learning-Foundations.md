# Machine Learning Foundations

Notes on the machine learning concepts I have learned and practiced so far.

## Core Concepts

### Features and Targets

In supervised learning, the data is separated into:

- `X` — the features given to the model
- `y` — the value or class the model is trying to predict

One thing I learned is that the target determines the type of problem, not the data type of the features.

### Classification and Regression

**Classification** is used when the target represents a class or category.

**Regression** is used when the target represents a numerical quantity where the difference between values matters.

This also affects how the model should be evaluated:

- Classification: accuracy and confusion matrix
- Regression: Mean Absolute Error (MAE)

## Training and Testing

I use training data to fit the model and keep test data separate to measure how well the model performs on unseen data.

A typical workflow is:

`data → features/target → train/test split → train model → predict → evaluate`

I have also worked with datasets that already provide separate training and testing files.

## Overfitting

I learned to compare training and testing performance instead of judging a model only by how well it performs on its training data.

A model can perform extremely well on training data while performing much worse on new data. This is overfitting.

For Decision Trees, I practiced controlling model complexity with parameters such as `max_depth`.

## Cross-Validation

Instead of repeatedly using the test set to choose model settings, I use cross-validation on the training data.

With 5-fold cross-validation, the training data is divided into five parts. The model is trained and validated multiple times, and the results are averaged.

This can be used to compare settings such as different tree depths before evaluating the final model on the test set.

## Data Preparation

I have practiced working with different dataset formats and structures, including:

- CSV, TXT, and Parquet files
- Datasets with and without headers
- Numerical and categorical features
- One-hot encoding
- Separate training and testing datasets

I also learned that preprocessing should be learned from the training data and then applied to the test data rather than allowing the test data to influence training.

## Data Leakage

Features should not contain information that directly or indirectly gives away the target.

I check the meaning of the columns before training instead of automatically using every available column as a feature.

## Decision Trees and Random Forests

I started with Decision Trees for both classification and regression.

I then learned how Random Forests combine multiple randomized Decision Trees instead of relying on a single tree. This can make predictions more stable and reduce some of the problems caused by an individual tree.

## Tools

- Python
- pandas
- scikit-learn
- Kaggle Notebooks

## Next

I am continuing to build on these foundations with model evaluation, preprocessing, and practical machine learning projects.
