# Fit the model and evaluate #

Now that you've defined a new model, fit it to the regular season basketball data.

Use the model you fit in the previous exercise (which was trained on the regular season data) and evaluate the model on data for tournament games (`games_tourney`).

## Instructions ##

* Fit the model to the `games_season` dataset, using `'team_1'`, `'team_2'` and `'home'` columns as inputs, and the `'score_diff'` column as the target.
* Fit the model using `1` epoch, 10% validation split and a batch size of `2048`.
* Evaluate the model on `games_tourney`, using the same inputs and outputs.

```python
# Fit the model to the games_season dataset
model.fit([games_season['team_1'], games_season['team_2'], games_season['home']],
          games_season['score_diff'],
          epochs=1,
          verbose=True,
          validation_split=0.1,
          batch_size=2048)

# Evaluate the model on the games_tourney dataset
model.evaluate([games_tourney['team_1'], games_tourney['team_2'], games_tourney['home']],
          games_tourney['score_diff'])
```

```
Train on 280960 samples, validate on 31218 samples
Epoch 1/1

  2048/280960 [..............................] - ETA: 18s - loss: 12.3681
 34816/280960 [==>...........................] - ETA: 1s - loss: 12.3641 
 67584/280960 [======>.......................] - ETA: 0s - loss: 12.2945
102400/280960 [=========>....................] - ETA: 0s - loss: 12.2708
137216/280960 [=============>................] - ETA: 0s - loss: 12.2600
172032/280960 [=================>............] - ETA: 0s - loss: 12.2468
206848/280960 [=====================>........] - ETA: 0s - loss: 12.2548
241664/280960 [========================>.....] - ETA: 0s - loss: 12.2812
276480/280960 [============================>.] - ETA: 0s - loss: 12.2833
280960/280960 [==============================] - 1s 2us/step - loss: 12.2829 - val_loss: 11.5521

  32/4234 [..............................] - ETA: 0s
1056/4234 [======>.......................] - ETA: 0s
1984/4234 [=============>................] - ETA: 0s
2752/4234 [==================>...........] - ETA: 0s
3616/4234 [========================>.....] - ETA: 0s
4234/4234 [==============================] - 0s 58us/step
Out[1]: 11.68496760502141
```