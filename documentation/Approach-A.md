# Approach A - PDDL / Classical Planning

## Motivation

The motivation was to develop an agent(s) that uses classical planning, by making calls to a solver using templated environment files, to act within the Pacman contest environment.

## Theory

**Classical Planning**, in the form of model-based planning, solves the problem of which action an agent should do by:

- **Specifying a model representing the problem (the state model)**, including:
  - a finite and discrete state space;
  - a known initial state;
  - a set of goal states;
  - actions applicable in each state;
  - a deterministic transition function;
  - positive action costs;
- **Making a call to a planner (using the state model), which returns a controller (i.e. a plan);**
- **Using this controller to act in the desired environment.**

This approach would utilise Planning Domain Definition Language (PDDL) to model the Pacman environment.

## Trade-offs

### Advantages:

- Requires much less programming (in the form of problem description), as opposed to many other AI methods.
- Can be extremely powerful in some circumstances.

### Disadvantages:

- Assumes a single-agent, fully-observable, deterministic, static environment.

## Special Note:

This specific approach was the only one which was not successfully implemented in any of the agents; this was primarily due to technical issues experienced in implementing the Metric-FF solver.

[Back to AI Approaches Overview](AI-Approaches-Overview)