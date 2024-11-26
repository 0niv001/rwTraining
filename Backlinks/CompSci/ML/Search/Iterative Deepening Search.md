Search algorithm that combines the good point of breadth first and depth first.

Avoids long or infinite paths, and finds one of the shortest solutions, without using a lot of memory.

Best used when all actions have the same cost, and is complete on finite acyclic state space.

It may seem wasteful to iterate the top nodes, but for a lot of state spaces, most of the nodes are in the bottom level so it does not matter as much.

Preferred method when state space is larger than can fit in memory and the depth of the solution is unknown.

The time complexity is O(b^d) when there is a solution, or O(b^m) when there is none. Each iteration of iterative deepening search generates a new level, in the same way that breadth-first search does, but breadth-first does this by storing all nodes in memory, while iterative-deepening does it by repeating the previous levels, thereby saving memory at the cost of more time.

It returns either a solution node; or failure, when it has exhausted all nodes and proved there is no solution at any depth; or cutoff, to mean there might be a solution at a deeper depth than l.

This is a tree-like search algorithm that does not keep track of reached states, and thus uses much less memory than best-first search, but runs the risk of visiting the same state multiple times on different paths.

If the IS-CYCLE check does not check all cycles, then the algorithm may get caught in a loop.

- Question
    - Some states are generated multiple times in iterative deepening search. Is this a problem? In what circumstances is it a good idea to use iterative deepening instead of breadth-first search?