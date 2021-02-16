# Approach E - Behaviour Trees

## Motivation

The motivation for this approach was to produce an agent which uses behaviour trees in order to act and make decisions within the Pacman contest environment.

## Theory

**Behaviour trees** are trees containing hierarchical nodes which control the flow of decision making of agents. These trees are defined as directed acyclic graphs with internal nodes corresponding with events/stimuli, and external nodes corresponding with behaviours (in contrast with hierarchical state machines whereby stimuli leads to states, rather than behaviours). The image below illustrates a simplistic behaviour tree for a two-armed robot (By Aliekor at English Wikipedia, CC BY-SA 3.0, https://commons.wikimedia.org/w/index.php?curid=39804218):

![BT_search_and_grasp](https://user-images.githubusercontent.com/50134351/96334793-0d210d80-10bf-11eb-990e-9f2df0065607.png)

## Application

An agent utilising a behaviour tree would be able smart and informed decisions which have been pre-programmed by the agent-designer. Possibilities for evolving behaviour would stem from manual supervision of matches in an effort to assess which stimuli should trigger certain behaviours. 

## Trade-offs

### Advantages:

- Behaviour trees can be programmed once and then can be used right away, i.e. behaviour tree implementation requires no pre-match training.
- Decisions can be informed by human intervention, effectively bestowing outsider knowledge/strategies onto the agent.
- Behaviour trees are so extremely effective in controlling agents within gaming environments (i.e. NPCs), that their usage is mainstream within the gaming AI community at large.
- Behaviour trees can be used in conjunction with AI decision making approaches (e.g. if A, then perform Monte Carlo Tree Search)

### Disadvantages:

- Behaviour trees require domain-knowledge to be hard-coded by the agent-designer, i.e. the agent is only as good as the agent-designer.
- Behaviour trees are really an instance of AI decision-making.

## Special Note:

This team understood that this is not strictly an AI method as defined within the project specifications, however given its usage within Agent 3, it required mentioning from an approach-perspective.

[Back to AI Approaches Overview](AI-Approaches-Overview)