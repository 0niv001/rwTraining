Adds depth limit to the depth first search. Advantage that it cannot follow an infinite path forever since the search can only go up to the limit.

If limit is less than the depth of the shallowest goal state, it will fail to find a solution.

Issue of setting the right depth limit is solved through Iterative deepening search.

The time complexity is O(b^l) and the space complexity is O(bl).