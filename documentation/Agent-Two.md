## Agent 2: Approximate Q-Learning

**Agent 2** utilises **Approximate Q-Learning [(Approach C)](Approach-C)** in order to act within the Pacman contest environment.

### Evolution:

- Agent 2 was initially planned to implement Classical Q-Learning approach, however both our testing and the research showed that this approach is better suited for very small grids (i.e. was not scalable to larger domains).
- After realising this, developing an agent utilising Deep Q-Learning was considered, however this approach was also unfeasible given the 15-second training time before each match being insufficient to train a deep neural network.
- Thus, Approximate Q-Learning was the only Q-Learning option left, and a rudimentary agent utilising this approach was designed in conjunction with tried and tested methods within the Pacman AI game literature available online.
- The development of Agent 2 into a more competent Pacman agent almost solely revolved around the trial and error regarding which features should be extracted in order to accurately represent the agent's surrounding environment as effectively as possible (these features are described in **Gameplay** below).
- The main challenge with Agent 2 is that the approximated Q-value was not proven to converge for all feature functions. Theoretically, the calculated Q-value (once converged) will be an optimal approximation of the optimal Q-value with regard to the choice of the feature function. 
- This leads to the secondary challenge of finding an appropriate feature function which provides an optimal representation of the agents' domain. By doing so, the resulting policy will be optimal, however, this task was far from trivial and was eventually abandoned.

### Gameplay:

- Agent 2 consisted of two separate sub-class agents: an offensive agent and a defensive agent, i.e. an agent acting as a Pacman and an agent acting as a ghost, respectively.
- The general strategy of this agent can be described as a balanced approach, possessing explicit offensive and defensive agents. 
- These two agents differed in their initial parameters and the features extracted to represent their surrounding environment; the specifics of which are explored in the subsections below.

#### Offensive Agent:

Features:

- **Bias:** weight bias
- **Successor score:** score value based on whether food is available in possible moves
- **Number of ghosts one step away:** calculates number of enemy ghosts one step away from agent
- **Distance from closest ghost:** calculates distance of closest ghost from agent
- **Distance from closest food:** calculates distance of closest food from agent
- **Whether agent is home:** whether agent is within home territory or not

Other parameters:

- **Carry Limit:** indicates the amount of food the agent (Pacman) should carry
- **Power Limit:** indicates whether it is safe to approach enemy ghosts after having eaten a power capsule

#### Defensive Agent:

Features:

- **Bias:** weight bias
- **Number of invaders:** calculates number of invaders (enemy Pacman) within home territory
- **Distance from middle:** calculates distance of the middle of the map from agent
- **Distance from closest invader:** calculates distance of closest invader (enemy Pacman) from agent
- **Scared distance:** distance of the closest invader from scared agent

Additionally, the training hyper-parameters (how will the agent's Q-function be structured? i.e. how will the agent learn? what are its priorities?), were tuned in an effort to optimise training for both agents; hyper-parameters described below:

- **Learning rate (alpha):** to what extent will new information be weighted higher than old information.
- **Exploration rate (epsilon):** to what extent will the agent explore actions versus exploit best-known actions.
- **Discount rate (gamma):** to what extent will a feature reward be discounted compared to a current reward.

### Further Improvements:

- Investigation into a larger set of features / performing a comprehensive analysis would provide more concrete indication of how each feature contributes to possible increase in win rates.
- Investigation into the use of auxiliary rewards for agents.
- Another possible improvement would be the combination of using Approximate Q-Learning in conjunction with another AI method.

[Back to Evolution and Experiments](Evolution-and-Experiments)