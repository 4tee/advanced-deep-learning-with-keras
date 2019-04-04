# Evaluate the model on the tournament test data #

The model you fit to the regular season data (`model`) in the previous exercise and the tournament dataset (`games_tourney`) are available in your workspace.

In this exercise, you will evaluate the model on this new dataset. This evaluation will tell you how well you can predict the tournament games, based on a model trained with the regular season data. This is interesting because many teams play each other in the tournament that did not play in the regular season, so this is a very good check that your model is not overfitting.

## Instructions ##

* Assign the `'team_1'` and `'team_2'` columns from `games_tourney` to `input_1` and `input_2`, respectively.
* Evaluate the model.

```python
# Get team_1 from the tournament data
input_1 = games_tourney['team_1']

# Get team_2 from the tournament data
input_2 = games_tourney['team_2']

# Evaluate the model using these inputs
model.evaluate([input_1, input_2], games_tourney['score_diff'])
```

```
  32/4234 [..............................] - ETA: 1s
1184/4234 [=======>......................] - ETA: 0s
2368/4234 [===============>..............] - ETA: 0s
3552/4234 [========================>.....] - ETA: 0s
4234/4234 [==============================] - 0s 46us/step
Out[2]: 11.649009290595183
```