# Evaluate the model on a test set #

After fitting the model, you can evaluate it on new data. You will give the model a new `X` matrix (also called test data), allow it to make predictions, and then compare to the known `y` variable (also called target data).

In this case, you'll use data from the post-season tournament to evaluate your model. The tournament games happen after the regular season games you used to train our model, and are therefore a good evaluation of how well your model performs out-of-sample.

The `games_tourney_test` DataFrame along with the fitted `model` object is available in your workspace.

## Instructions ##

* Assign the test data (`seed_diff` column) to `X_test`.
* Assign the target data (`score_diff` column) to `y_test`.
* Evaluate the model on `X_test` and `y_test`.

```python
# Load the X variable from the test data
X_test = games_tourney_test['seed_diff']

# Load the y variable from the test data
y_test = games_tourney_test['score_diff']

# Evaluate the model on the test data
model.evaluate(X_test, y_test)
```

```
     32/804 [>.............................] - ETA: 0s
    804/804 [==============================] - 0s 55us/step
    Out[1]: 10.06973339669147
```