Each node in a search tree corresponds to a state, and edges in the tree are actions.

Root of the tree is the initial state of the problem.

The search tree can have many paths to a state, all nodes will have a path back to the root.

New nodes created from the results are called child nodes.

Unexpanded nodes are the frontier of the search tree, whilst any state that has had a node generated for it has been reached.

The frontier separates two regions of the state space graph:

- An inner part where every state has been expanded
- An outer part where the states have not been reached.