# Approach C - Approximate Q-Learning

## Motivation

The motivation for this approach was to produce approximate Q-learning agent(s) (both offensive and defensive) which learns feature-weights of states (described below) that enable the agent to act within the Pacman contest environment. 

## Theory

**Approximate Q-Learning** is a means of approximating the Q-functions used in traditional/simple Q-learning. This method utilises reward shaping (providing an agent with useful, intermediate rewards) in addition to function approximation in order to reduce a once-exponentially large state space into a more feasible domain. This is done by:

1. **Extracting features deemed necessary for the problem task;**

2. **Performing updates on the weights of said features;**

3. **Estimating Q-values by summing features and their weights.**

## Trade-offs

### Advantages:

- Enables the feasible implementation behind Q-learning without the exponentially-increasing domain size problem, i.e. reduces the size of the Q-table.
  - This advantage is especially salient given the 1 second time restriction for agent actions: our agents do not have the time, nor the computational  capability, to run simple Q-learning.
- Forces consistent behaviour patterns, i.e. agents using Q-learning are more likely to act in a consistent manner in similar situations (chasing an enemy, eating food, running from an enemy, etc.).
- Allows the designers to play a hand in deciding which aspects of states within the Pacman environment are important for our agent, i.e. closest food to agent? Number of enemies within a certain radius? These features are all programmable into our feature vectors.

### Disadvantages:

- Requires complex feature extraction, the success of which is determined purely by trial and error; domain-knowledge; research papers; intuition; etc.
  - Additionally, this reduces the so-called "generality" of our agent, as human-input in the form of domain-knowledge is required to implement approximate Q-learning.
- The accuracy of rewards is reduced as the true/optimal reward function may not be linearly formed within the features extracted.

[Back to AI Approaches Overview](AI-Approaches-Overview)