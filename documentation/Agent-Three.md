## Agent 3: A\* Heuristic Search and Behaviour Trees

**Agent 3** utilises **A\* Heuristic Search ([Approach D](Approach-D))** as well as aspects inspired by **Behaviour Trees ([Approach E](Approach-E))** in order to act within the Pacman contest environment.

### Behaviour Tree:

![Behaviour Tree](https://user-images.githubusercontent.com/50134351/96994136-fa538080-1577-11eb-803d-0e8ef5d94d06.PNG)

### Evolution:

- Agent 3, in its initial form, was coded to investigate the performance of using A\* heuristic search plus a simple decision tree, as well as to provide a baseline performance for comparison for the other agents which were being investigated at the time.
- From then onward, different ideas for improvement were investigated and, one after another, Agent 3's performance in the competition increase; there improvements arose from questions such as:
  - Can we prevent our agent from being eaten when they search for food?
  - What should our agent to when no optimal action exists?
  - How can our agent avoid a deadlock with an enemy agent?
  - How should our agent act knowing it will be eaten?
- The major challenge in programming Agent 3 was in the design its behaviour protocols (see **Gameplay** below); this process required extensive research which began with investigating the simple mechanics of the baseline agent, and ended with devising complex strategies to combat smarter opponents (inspiration of which was gleaned from other agents being built at the time, as well as wider research papers on the topic).

### Gameplay:

- Agent 3 acts as a dual offensive-defensive agent, however if focuses primarily on offensive strategies. Thus, the agent immortalises the saying *"the best defence is a good offence"*.
- The agent general strategies are controlled by behaviour tree-like mechanisms (see **Behaviour Tree** above).
- The agent acts in one of five various ways depending on the environment and its past actions, each of which have been generalised/simplified below:
  1. **Eat enemy food:** basic offensive strategy to find nearest food (acting in consideration of teammate's position)
  2. **Find different attack path:** secondary offensive strategy to find point of attack farthest away from current position
  3. **Return home:** agent finds shortest path to home territory
  4. **Escape:** primary evasive strategy to avoid enemy ghost (returns home; eats capsule; etc.)
  5. **Defend remaining food:** sole defensive strategy to chase enemy offensive agents in territory

The following is a list of improvements that eventually became the behaviour protocols to which we attribute the agent's success:

- **Different Path Protocol:** agent finds different path (than current) to attack enemy agents
- **Enemy Avoidance Protocol:** agent avoids enemies when searching for paths to food

![Enemy Avoidance Protocol](https://user-images.githubusercontent.com/50134351/97100460-e890eb00-16e7-11eb-9ad1-2ef84c3091ea.gif)

- **DRP (Don't Repeat the Past) Protocol:** agent finds different attack path if performing repeated actions

![DRP Protocol](https://user-images.githubusercontent.com/50134351/97100764-293e3380-16eb-11eb-8f5b-b80b3aa21979.gif)

- **Last Resort Protocol:** agent consumes capsule if it cannot return home whilst being chased

![Last Resort Protocol](https://user-images.githubusercontent.com/50134351/97100256-ba121080-16e5-11eb-8e60-cbb6ccb85c06.gif)

### Further Improvements:

- Investigation into game theory with regards to multi-agent systems could have provided further insight into better strategies.
- Possible integration with approaches other than A\* heuristic search may have provided overall better agents.
- Investigation into developing a more balanced team, i.e. designing both an offensive and defensive agent, may have yielded better competition results.

[Back to Evolution and Experiments](Evolution-and-Experiments)