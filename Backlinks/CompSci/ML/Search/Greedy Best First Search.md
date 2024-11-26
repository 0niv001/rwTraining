Algorithm that expands the frontier node that appears to be closest to a goal according to the heuristic function, so with the lowest h(n) value

Evaluation function f(n) = h(n).

Values of h cannot be computer from the problem description themselves, and since it takes world knowledge to know h, it is a useful heuristic.

Solution will not always be optimal.

Algorithm is called greedy, since on each iteration it tries to get as close to a goal as it can, which can lead to worse results.

Only evaluation function used is the heuristic function.

Complete in finite spaces, but not in infinite ones.

Worst case time and space complexity is O(|V|).

Depending on the heuristic function, complexity can be reduced up to O(bm).