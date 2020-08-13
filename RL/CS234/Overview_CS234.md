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

