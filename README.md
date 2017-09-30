# A3C Continuous Reinforcement Learning
Tensorflow implementation of the asynchronous advantage actor-critic (A3C) reinforcement learning algorithm [(paper)](https://arxiv.org/pdf/1602.01783.pdf) for continuous action space. Code is mostly based on Morvan Zhou [(github)](https://github.com/MorvanZhou/Reinforcement-learning-with-tensorflow).

## Components
* ACNet: This class contains the actor-critic neural network that estimates an action given a certain state and a value for each state. For continuous action states the action is given as an expected value mu and variance sigma. 
* Worker: The A3C algorithm employs multiple workers which have their own environment and ACNet and train on these asynchronous. Every few steps they update their weights to the global ACNet.
* Main: The main function creates the global ACNet and multiple workers. They start training until a defined number of training episodes is reached. Reward will be plotted over all steps.

## Results

Pendulum environment before training:

![before](gifs/episode1.gif)


After 1500 episodes:

![after](gifs/episode1500.gif)
