# Approach B - Value Iteration

## Motivation

The motivation for this approach was to produce an agent which utilises value iteration to provide optimal policies for acting within the Pacman contest environment.

## Theory

**Value Iteration** is an offline algorithm which computes an optimal policy for a Markov Decision Process (MDP). The algorithm does so by updating the value function (Bellman equation) through iterating over Q-functions until they converge to optimal values. Using these optimal Q-values, the action which maximises the highest expected reward is selected (aka **policy extraction**).

## Trade-offs

### Advantages:

- Value iteration will converge towards optimal Q-values.
- Solves MDPs with small state spaces efficiently.

### Disadvantages:

- Requires that we know the MDP.
- Solving MDPs using value iteration requires a large training time before it arrives to a complete (near-optimal) policy for the environment.
- An agent acting based on a policy computed by value iteration is a reflex agent, rather than an agent which acts in response to stimuli in the environment.

[Back to AI Approaches Overview](AI-Approaches-Overview)