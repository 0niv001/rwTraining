Always selects and expands the shallowest node in the frontier.

The first solution that it will find, will always be the shortest one, since it looks at all the paths.

Systematic search that is complete even on infinite state spaces.

Uses a queue system, FIFO to store the nodes in a frontier.

Reached can be a set of states since once we have reached one, we cannot find a better path to it, allowing us to do an early goal test, checking for solution as soon as node is generated.

Drawback is that sets become very large and algorithms run out of memory on difficult search problems, additionally it’s time complexity is O(B^d), making it exponential.

Execution time can also become a massive problem.

Best used when all actions have the same cost.

In general exponential complexity search problems cannot be solved by uninformed search