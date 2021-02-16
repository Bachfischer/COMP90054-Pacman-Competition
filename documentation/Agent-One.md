## Agent 1

**Agent 1** utilises **Value Iteration ([Approach B](Approach-B))** and **A\* Heuristic Search ([Approach D](Approach-D))** in order to act within the Pacman contest environment.

### Evolution:

- Before explicitly build the value iteration used in Agent 1, search algorithms such as BFS-search and A\* were both coded, with the latter being used in Agent 1's implementation.
- When designing the value iteration algorithm, the main point of focus was constructing the reward function, which was based upon whether a cell contained food or how far an enemy agent was, for offensive and defensive agents, respectively.
- The design of this reward function was the primary challenge in building Agent 1, which is largely a problem of how to balance risk versus reward (the work on this problem consumed much of the time working on this agent), more specifically, how to set fixed weights so that our agent exhibits behaviours such as:
  - eating food; avoiding corners; avoiding the enemy; chasing the enemy; returning home after eating food; etc.
- These behaviours are extremely difficult to elicit from an agent without the use of behaviour trees.
- A secondary challenge was that the number of iteration used in the algorithm caused the agent's decision making to drastically slow down; additionally, the agent was slowed when larger maps were played on.

### Gameplay:

Agent 1 consists of both an offensive and defensive agent, meaning that the general strategic approach is a balanced one. The differing strategies between the two are outlined below:

#### Offensive Agent:

- Utilises A\* Heuristic Search to reach opposite end of the map;
- Value iteration is then used to find the most suitable food to eat.

#### Defensive Agent:

- Attempts to reach the border between home and enemy territory;
- Proceeds to chase enemy Pacman agents using A\* Heuristic Search.

### Further Improvements:

- Investigation into how to force the offensive agent to retreat back into home territory by altering the parameters of the reward function (as opposed to utilising a behaviour tree), i.e. optimal manipulation of the weights.
- Investigation into using non-fixed weights for different situations to calculate the reward function rather than using deterministic weights.

[Back to Evolution and Experiments](Evolution-and-Experiments)