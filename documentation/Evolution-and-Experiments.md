# Evolution and Experiments

The following is a list of agents that were developed throughout this project. A very brief description of each agents' evolution is provided, in addition to which files they correspond to:

1. [Agent 1: Value Iteration and A\* Heuristic Search](Agent-One)

**Agent 1** implements Value Iteration as its primary AI approach; A\* Heuristic Search as its supplementary approach.

**Agent 1**'s development was primarily centred around designing the reward functions for the offensive and defensive agents.

The code for **Agent 1** is contained within `myTeam_value_iteration.py`.

2. [Agent 2: Approximate Q-Learning](Agent-Two)

**Agent 2** implements Approximate Q-Learning as its primary AI approach.

**Agent 2** was developed after investigating all three possible Q-learning approaches (Classical Q-Learning and Deep Q-Learning), with Approximate Q-Learning labelled as the most appropriate of the three.

The code for **Agent 2** is contained within `myTeam_approx_q_learning.py`.

3. [Agent 3: A* Heuristic Search and Behaviour Trees](Agent-Three)

**Agent 3** implements A\* Heuristic search and Behaviour Trees as its primary AI approaches.

**Agent 3** was developed as a baseline agent for use of comparison with the other agents being built at the time, however, its success in some competitions lead to its further development. Eventually, **Agent 3** was chosen to be the primary agent for our team, and thus, it took part in both the preliminary and final competition rounds.

The code for **Agent 3** is contained with `myTeam.py` (additionally, the version of **Agent 3**'s code which was submitted for the preliminary round is contained within `myTeam_preliminary_submission.py`).

## Comparison

The table below provides a quantitative comparison between each of the agents, containing the win-rates and average scores of each agent against the baseline team on each map (with 10 matches per map for each agent):

|       Map:       | Agent 1: Win Rate | Agent 1: Av. Score | Agent 2: Win Rate | Agent 2: Av. Score | Agent 3: Win Rate | Agent 3: Av. Score |
| :--------------: | :---------------: | :----------------: | :---------------: | :----------------: | :---------------: | :----------------: |
|   alleyCapture   |        50%        |        0.6         |        90%        |        5.4         |        70%        |        3.6         |
|   bloxCapture    |       100%        |        13.3        |       100%        |        25.1        |       100%        |        36.2        |
|  crowdedCapture  |       100%        |        20.2        |        70%        |        15.9        |        80%        |        37.1        |
|  defaultCapture  |        90%        |        2.8         |       100%        |        11.1        |       100%        |        18.9        |
|  distantCapture  |        60%        |        2.2         |       100%        |        12.8        |        90%        |        14.7        |
|   fastCapture    |        20%        |        0.6         |       100%        |        4.5         |        80%        |        5.1         |
|   jumboCapture   |         —         |         —          |       100%        |        64.1        |       100%        |       156.8        |
|  mediumCapture   |       100%        |        14.9        |       100%        |        21.5        |       100%        |        38.6        |
|  officeCapture   |         —         |         —          |       100%        |        22.5        |       100%        |       123.2        |
| strategicCapture |        90%        |         6          |       100%        |        21.1        |        90%        |        31.2        |
|   testCapture    |         —         |         —          |         —         |         —          |         —         |         —          |
|   tinyCapture    |         —         |         —          |       100%        |        5.4         |        90%        |        3.6         |
|    **TOTAL:**    |        76%        |        7.6         |      **96%**      |        19.0        |        91%        |      **42.6**      |

(**Note:** an em-dash represents that every match within a map was a tie)

## Discussion

As illustrated in the table above, **Agent 2** (Value Iteration and A\* Heuristic Search) possesses the highest total win rate of 96%, however **Agent 3** (A* Heuristic Search and Behaviour Trees) holds the highest total average score 42.6. The drastic difference between **Agent 3**'s average scores versus the other agents can most likely be attributed to its overly aggressive play-style, whereas the other agents use balanced strategies. This means that when the map and/or the circumstances of the game favour a more balanced approach, **Agent 2** is more likely to win, even if the average score is lower in comparison to **Agent 3**. In contrast, when the circumstances allow for an aggressive strategy, **Agent 3** is more likely to win and achieve higher average scores at the same time.

[Back to Home](Home)