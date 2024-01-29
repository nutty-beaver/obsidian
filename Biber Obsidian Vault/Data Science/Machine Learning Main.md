![[machine learning]]

Machine learning is a branch of computer science where you predict an output by creating a model from a dataset, learning its patterns and correlation with your assigned dependent ([[label]]) and independent variables ([[feature]])

# Models
## Building models

### Steps to build model using `scikit-learn`
- **Define** what type of model to use (e.g. [[linear regression]], [[decision tree]], [[random forest]])
- **Fit** or capture patterns from the data
- **Predict**
- **Evaluate** how accurate and valid the predictions are

```python
from sklearn.tree import DecisionTreeRegressor

# Define model. Specify a number for random_state to ensure same results each run
model = DecisionTreeRegressor(random_state=1)

# Fit model - X are the features and y is label
# X and y are both dataframes
model.fit(X, y)

# Predict results
predicted_y = model.predict(X)
```

## Validating models
You need to validate your models to measure how accurate your predictions are.  This can be done by computing the `mean absolute error` which is equal to absolute difference of `actual label (y)` and `predicted label (predicted_y)`

```python
from sklearn.metrics import mean_absolute_error

MAE = mean_absolute_error(y, predicted_y)
```

If you validate your model with your training data, expect it to give you 100% accuracy. To prevent this, you may want a separate training and testing data. You can do this manually but `sklearn` have a function that automatically splits your data

```python
from sklearn.model selection import train_test_split
from sklearn.tree import DecisionTreeRegressor
from sklearn.metrics import mean_absolute_error

# splits the data for training and validation
train_X, val_X, train_y, val_y = train_test_split(X, y)

# create model from training data
model = DecisionTreeRegressor()
model.fit(train_X, train_y)

# determine the prediction from validation features (X)
val_prediction = model.predict(val_X)

# determine the mean absolute error between actual data
# prediction on validation data and 
MAE = mean_absolute_error(val_y, val_prediction)
```

## Overfitting and Underfitting
Clothes tailor-fit for you obviously would suit you, but it would not be for everybody else. Just like with models, overfitted models may just represent your test data, making almost perfect predictions with it but would give bad predictions when tested with data outside your training dataset or "real life data". This happens when the model get *too deep* with the data.

Underfitting is the opposite; making your model too generic or broad. Getting the [[goldilock's zone|sweet spot]] might involve a bit of trial and error on how deep you want your model to train on the data set.

# Data Preparation
## Missing Values
--

## Categorical Variables
--

## Pipelines