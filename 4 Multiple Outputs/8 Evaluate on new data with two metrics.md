# Evaluate on new data with two metrics #

Now that you've fit your model and inspected its weights to make sure they make sense, evaluate your model on the tournament test set to see how well it does on new data.

Note that in this case, Keras will return 3 numbers: the first number will be the sum of both the loss functions, and then the next 2 numbers will be the loss functions you used when defining the model.

Ready to take your deep learning to the next level? Check out "Convolutional Neural Networks for Image Processing".

## Instructions ##

* Evaluate the model on `games_tourney_test`.
* Use the same inputs and outputs as the training set.

```python
# Evaluate the model on new data
model.evaluate(games_tourney_test[['seed_diff', 'pred']],
               [games_tourney_test[['score_diff']], games_tourney_test[['won']]])
```

```
 32/804 [>.............................] - ETA: 0s
800/804 [============================>.] - ETA: 0s
804/804 [==============================] - 0s 86us/step
Out[1]: [9.685116468970456, 9.11585681592647, 0.5692595753503676]
```