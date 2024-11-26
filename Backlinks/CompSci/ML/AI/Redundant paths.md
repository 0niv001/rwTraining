A repeated state can be created by things like cycles and infinite loops.

Redundant paths should not be considered when looking for optimal paths.

3 approaches to redundant paths:

1. Remember all previously reached states, detecting all of them, and only keeping the viable ones -
    1. Good for when there are many redundant ones
    2. Chosen when table of reached states will fit into memory
2. Do not worry about it - in some formulations it is rare for 2 paths to reach the same state.
    1. Helps save memory in space
    2. GRAPH SEARCH - checks for redundant paths
    3. TREE SEARCH - does not check for redundant paths.
3. Check for cycles but not redundant paths in general, does not take up memory as we just follow the chain of parents.