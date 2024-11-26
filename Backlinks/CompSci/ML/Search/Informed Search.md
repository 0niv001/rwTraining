These algorithms have an evaluation function that guides the search by computing a score. 

[[Heuristics]] function is used as part of the evaluation function. 

These strategies go towards a promising part of the search space by heuristic function - hints -, allowing them to perform better than uninformed search strategies.

Heuristics are functions from a state to a score, where each heuristic is specific to a specific problem.

Heuristic functions are denoted h(n)

h(n) = Estimated cost of the cheapest path from the sate at node n to a goal state.

How the heuristic is used depends on which informed search strategy is chosen.

e.g. In route finding problems we can estimate the distance from current state to a goal by computing straight line distance on map between two points.