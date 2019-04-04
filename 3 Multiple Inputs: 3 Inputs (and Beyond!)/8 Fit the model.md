# Fit the model #

Now that you've enriched the tournament dataset and built a model to make use of the new data, fit that model to the tournament data.

Note that this model has only one input layer that is capable of handling all 3 inputs, so it's inputs and outputs do not need to be a list.

Tournament games are split into a training set and a test set. The tournament games before 2010 are in the training set, and the ones after 2010 are in the test set.

## Instructions ##

* Fit the model to the `games_tourney_train` dataset using 1 epoch.
* The input columns are `'home'`, `'seed_diff'`, and `'pred'`.
* The target column is `'score_diff'`.

```python
# Fit the model
model.fit(games_tourney_train[['home', 'seed_diff', 'pred']],
          games_tourney_train['score_diff'],
          epochs=1,
          verbose=True)
```

```
Epoch 1/1

  32/3168 [..............................] - ETA: 11s - loss: 12.3603
 800/3168 [======>.......................] - ETA: 0s - loss: 9.5943  
1568/3168 [=============>................] - ETA: 0s - loss: 9.4716
2336/3168 [=====================>........] - ETA: 0s - loss: 9.3209
3104/3168 [============================>.] - ETA: 0s - loss: 9.2664
3168/3168 [==============================] - 0s 102us/step - loss: 9.2360
Out[1]: <keras.callbacks.History at 0x7f8065d2df28>
```