# Bicycle Trajectory Forecasting in Bologna

In this repository one can find the notebooks I have developed as a final project for the PhD course in Applied Machine Learning (Basic + Advanced).
Using a database of bicycle trajectories recorded in Bologna during the spring and summer of 2017, we wish to predict the next location a person will visit, provided the recent history of visited locations.
Our locations are defined as squares on a grid (a.k.a. cells, characters), with corners at the north-west (44.53518 N, 11.26029 E) and at the south-east (44.46417 N, 11.40243 E), and the tracks are in principle timed sequences with a cell index sampled every 10 s.

## Table of contents:

1. Data preprocessing: in this notebook the data are analysed and prepared for the ML algorithms, in particular by creating sequences of fixed length from the original trips.
2. Deep Neural Network as a regressor: in this notebook, the problem is framed as a regression (extrapolation), and tackled with a Deep Neural Network. The final accuracy is roughly $53 \%$.
3. Deep Neural Network as a classifier: in this notebook the problem is framed as a classification task, and a DNN is trained to solve it, making use of a dropout mechanism to improve the generalisation capabilities. This approach achieves an accuracy of roughly $\approx 69 \%$.
4. Decision Tree as a classifier: in this notebook the classification problem is approached with a Decision Tree, to test the DNN against it. An optimal accuracy of $\approx 71 \%$ is obtained with a tree of depth $\approx 30$ layers.

For all algorithms, the training is performed using the data from the month of May, while the reported accuracies are obtained on independent data from the same dataset but considering the month of June.