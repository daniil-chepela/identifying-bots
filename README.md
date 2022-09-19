# identifying-bots
Identification of bots annotating data on Amazon Mechanical Turk crowdsourcing marketplace

This jupyter notebook proposes my solution to https://github.com/1712n/challenge/issues/77

First of all, the program runs recurrent neural network that classifies text based on data with incorrect labels. After that cleanlab library is used to identify the labels based on obtained probabilities. Then the ID of annotators who made mistakes are analyzed and annotators with the higest percentage of incorrect answers are considered as bots.

list of bot ID = [
  '',
  '',
  '',
  '',
  ''
]

It would be helpful to read [this article](https://l7.curtisnorthcutt.com/confident-learning) to better understand the algorithm behind cleanlab library

> The central idea is that when the predicted probability of an example is greater than a per-class-threshold, we confidently count that example as actually belonging to that threshold’s class. The thresholds for each class are the average predicted probability of examples in that class. 

[Cleanlab documentation](https://docs.cleanlab.ai/stable/index.html)

[Cleanlab GitHub](https://github.com/cleanlab/cleanlab)
