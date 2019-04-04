# Evaluate the model #

Now that you've fit your model and inspected it's weights to make sure it makes sense, evaluate it on the tournament test set to see how well it performs on new data.

## Instructions ##

* Evaluate the model on `games_tourney_test`.
* Use the same inputs and outputs as the training set.

```python
# Evaluate the model on the tournament test data
model.evaluate(games_tourney_test[['seed_diff', 'pred']],
  		  games_tourney_test[['score_1', 'score_2']])
```

```
 32/804 [>.............................] - ETA: 0s
804/804 [==============================] - 0s 51us/step
Out[1]: 8.986760239102948
```