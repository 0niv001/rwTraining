We can evaluate algorithms performance in 4 main ways:

1. Completeness: Is it guaranteed to find a solution when there is one, and report a failure when there isn’t
    1. Can it go through all the states reachable from the initial state - Difficult in infinite spaces.
    2. Systematic in a way it explores infinite space, making sure it can reach the initial state somehow.
2. Cost optimality: Does it find a solution with the lowest path cost of all solutions
3. Time complexity / [[Asymptotic Notation]]: How long does it take to find a solution. 
4. Space complexity: How much memory it takes

Complexity can be measured in terms of:

- depth (number of actions in optimal solution).
- m: maximum number of actions in any path.
- b : branching factor / number of successors of a node that need to be considered.