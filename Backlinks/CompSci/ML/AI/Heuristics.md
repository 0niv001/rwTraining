There are different ways to compare heurisitcs

Analytical (Math comparison)

Domination: h2 is always ≥ than h1, therefore it must be more accurate

- Better accuracy, means that the search performs better.
- Not useful in general as we cannot always prove than one h is > than another.

Empirical (Measuring behaviour)

Measure Effective branching factor of each h in experiment and compare the two numbers.

- H with smaller EBF is better at guiding search.
- Combined with depth it can be used to estimate how many nodes A* search is likely to expand.

## Relaxation

Looks at taking away some rules of a problem to create a new problem that is easier to solve.

A problem with fewer restrictions on the actions is called a relaxed problem.

The state-space graph of a relaxed problem is a supergraph of the original state space because the removal of restrictions creates added edges in the graph.

Any optimal solution in the original problem, is by definition also a solution in the relaxed problem.

The relaxed solution might also have better solutions if the added edges provide shortcuts.

Cost of an optimal solution to a relaxed problem is an admissible heuristic for the original problem.

Because derived heuristic is exact cost for the relaxed problem, it needs to obey the triangle inequality and so it is also consistent.

We can derive relaxed problems by removing conditions from the original problem definition.