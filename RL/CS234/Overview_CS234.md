# Overview

Review What I learned from CS234. Go over all slides.

## Lecture 1

### Introduction to RL

- Sequential Decison Processes
  - Markov Assumption : Actions influence future observations
    - Fully observable Markov : S_t = O_t
    - Partially Observable : Agent state is not the same as the world state

  - Bandits : Actions have no influence on next observations. No delayed rewards.

- How the World changes
  - Deterministic
  - Stochastic

- Components
  - Model : How the world changes in response to agent's action
  - Policy : F : s → a
  - Value function : Future rewards from being in a state and/or action when following a particular policy.

- Key challenges
  - Planning
  - Exploration vs Exploitation

## Lecture 2

### Making decisions Given a Model of the World

- Markov Process
  - Memoryless random process
  - Is not about rewards or actions, but considering only state transitions.

- Markov Reward Process
  - Markov Chain + rewards
  - Does not consider Actions

- Markov Decision Process
  - Markov Reward Process + Actions

- MDP Policies
  - What action to take in each state
  - Evaluation : Bellman backup

- MDP Policy Iteration

- State-Action Value = Q

- Policy Iteration & Value Iteration
  - Bellman Operations

## Lecture 3

### Policy Evaluation Without True MDP models

- Dynamic Programming
  - __Bootstrapping__
  - __Requires__ model of MDP

- Monte Carlo Policy Evaluation
  - No MDP dynamics / No bootstrapping
  - Only available for _episodic_ MDPs

- __First-Visit__ Monte Carlo
  - An _unbiased_ estimator

- __Every-Visit__ Monte Carlo
  - A _biased_ estimator

- Temporal Difference Learning
  - Bootstrapping & Samples

- Metrics to evaluate & compare algorithms

- MC Off Policy Evaluation

## Lecture 4

### Model free control

- On-Policy vs Off-Policy
  - On-Policy : Direct experience. Evaluate a policy from data by _that policy._
  - Off-Policy : Evaluate a policy from data by a _different policy_

- Policy Evaluation with Exploration
  - e-greedy
  - Greedy in th Limit of Exploration (GLIE)

- Monte Carlo Online Control

- SARSA Algorithm

- Q-Learning

- Maximization Bias
  - Double Q-Learning

## Lecture 5

### Value Function Approximation

- Represent a (state-action/state) value function with a parameterized function instead of a table

- Function approximators
  - linear combinations
  - NN
  - Decision trees
  - KNN
  - Fourier / wavelet bases

- Stochastic Gradient Descent

- Don't have access to an oracle to tell true V_pi(s)

- Monte Carlo Value Function Approximation

- Temporal Difference learning

- Control using Value Function Approximation
  - Q learning

## Lecture 6

### CNNs and Deep Q Learning

- DNN
  - Linear + Non-linear

- DQN
  - Replay

- Improvements
  - Double DQN
  - Prioritized Replay
  - Dueling DQN
    - Advantage function

- Practical Tips
  - LR scheduling is beneficial : Try high LR in initial exploration period
  - Consider Double DQN

## Lecture 7

### Imitation Learning in Large State Spaces

- Reward shaping
  - Rewards that are dense in time

- Learning from demonstrations
  - Behavioral Cloning
  - Inverse Reinforcement Learning
  - Apprenticeship Learning
  - Maximum Entropy Inverse RL

## Lecture 8

### Policy Gradient

- Find policy π with the highest value function V^π

- Policy based RL can learn stochastic policies

- Evaluation
  - Episodic : Start value of the policy
  - Continuing : Average value of the policy / Average reward per time-step

- Policy Gradient

- Score function and policy gradient theorem
  - Compute policy gradient analytically
  - Define Score function

- Policy Gradient Algorithms and Reducing Variance

- Monte-Carlo Policy Gradient (REINFORCE)

## Lecture 9

### Policy Gradient 2

- Desired properties of a Policy Gradient RL algorithm
  - Converge quickly to a local optima
  - Monotonic improvement

- Choosing the baseline : Value Functions

- Actor-critic method
  - Estimate of V/Q is done by a critic

- Updating the Parameters

- Step Sizes
  - Auto-Step-Size selection

- Trust regions

- TRPO Algorithm

## Lecture 10

### Policy Gradient 3

*_Review of previous classes_*

## Lecture 11

### Fast Reinforcement Learning

