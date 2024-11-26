For recursive algorithms to work the smaller subproblems need to arrive at the base case. 
We need to make the subproblems progressively smaller

**Rules of recursion:
1. Each recursive call should be on a smaller instance of the same problem, that is a smaller subproblem.
2. The recursive calls must eventually reach a base case, which is solved without further recursion.

### Improving efficiency of recursive functions.
Recursion can be a good way to solve problems and many algos lend themselves to recursive solutions.  However they can be inefficient in terms of both time and space (Stack overflow). 

Memoization can be used to save the computer time when making identical function calls- It’s a form of caching that remembers the results of a function call with certain inputs in a lookup table

We can use an iterative technique called bottom up approach, where the computer solves the sub problems first and then uses the partial results to get to the final results.



