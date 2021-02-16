# Approach D - A* Heuristic Search 

## Motivation

The motivation for this approach was to produce agents which utilise A* heuristic search to accomplish goals within the Pacman contest environment.

## Theory

**A\*  ("A star")** is a heuristic search algorithm which generates a lowest-cost path tree from the start node to the goal node. A\* utilises a function *f(n)* which provides an estimate of the total cost of a path from node *n*. The function *f(n)* is calculated as *f(n) = g(n) + h(n)*, whereby *g(n)* is the cost to reach node *n*, and *h(n)* is the estimated cost from *n* to the goal node (requiring a heuristic cost function). A* is complete for safe heuristics and optimal for admissible heuristics.

## Application

An agent utilising A\* heuristic search would require additional techniques/methods to be implemented in conjunction with A\*, as this approach provides a baseline solution for an agent reaching its goals, but it does not implicitly define what those goals are. Thus, the additional technique/method would have to define these goals and then pass them to the agent in order for A\* to then execute the path to said goal.

## Trade-offs

### Advantages:

- A\* is complete for safe heuristics; optimal for admissible heuristics.
- Easy to quickly code an A\* algorithm.

### Disadvantages:

- A\* can be slow depending on which heuristic is used and the size of the search space; worst-case time complexity is *O(b^d)* (*b* = branching factor; *d* = goal depth). Additionally, it's worst-case space complexity is also *O(b^d)* (which consumes a lot of memory).

[Back to AI Approaches Overview](AI-Approaches-Overview)