# Q-Learning in short-swing trading

An implementation of Q-learning applied to short-swing stock trading. The model uses n-day windows of closing prices to determine if the best action to take at a given time is to buy, sell or sit.

## How to run

To get some real stock data from Alpha Vantage, run the following code:
```
python fetchdata.py
```

To train the model, make a directory called model first, and then train. Here, I give an
example of training on the Google stock data with 10-day windows of closing prices and 
200 episodes of simulation.

```
mkdir model
python train.py GOOGL_20190516 10 200
```

Then evaluate the model and get the total-profit:
```
python evaluate.py GOOGL_20190516 model_ep200
```

## References

[Deep Q-Learning with Keras and Gym](https://keon.io/deep-q-learning/) - Q-learning overview and Agent skeleton code