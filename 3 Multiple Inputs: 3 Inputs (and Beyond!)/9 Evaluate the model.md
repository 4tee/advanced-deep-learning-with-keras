# Evaluate the model #

Now that you've fit your model to the tournament training data, evaluate it on the tournament test data. Recall that the tournament test data contains games from after 2010.

## Instructions ##

* Evaluate the model on the `games_tourney_test` data.
* Recall that the model's inputs are `'home'`, `'seed_diff'`, and `'prediction'` columns and the target column is `'score_diff'`.

```python
# Evaluate the model on the games_tourney_test dataset
model.evaluate(games_tourney_test[['home','seed_diff','prediction']], 
               games_tourney_test['score_diff'])
```

```
  32/1066 [..............................] - ETA: 0s
1066/1066 [==============================] - 0s 73us/step
Out[2]: 9.07315489498804
```