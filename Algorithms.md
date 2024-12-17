Are evaluated using [[Asymptotic Notation]]
# Sorting
- Keys - What we want to sort. 
- Input - The array. 
- Swap function - Function that swaps the location of 2 items in an array. 

**Types of sorting algorithms**
- [[Merge sort]]
- [[Bubble sort]]
- [[Insertion sort]]
- [[Heap sort]]
- [[Selection sort]]
- [[Quick sort]]
## Searching
**Types of search algorithms**
[[Linear Search]]
[[Binary Search]]

*[[Tree Search]]and Graph search:*
- [[Best First Search - Graph]]

*[[Uninformed Search]]*
- [[Breadth First Search]]
- [[Depth First Search]]
- [[Depth Limited Search]]
- [[Iterative Deepening Search]]

*[[Informed Search]]*
- [[Greedy Best First Search]]
- [[A Search]]

Search algorithms need a data structure to keep track of the search tree.

Node in the tree is represented by a data structure with 4 components:
1. State: State to which the node corresponds. 
2. Parent: node that generated current one. 
3. Action: action applied to parent to generate this node. 
4. Path-Cost: cost of path from initial state to this node.

To store the frontier we use queues given these frontier operations:
- is_empty: T only if there are no nodes in frontier
- pop: removes and returns top node from frontier
- top: returns top node from frontier
- add: inserts node into proper place in the queue

In search algorithms 3 kinds of queues are used:
1. Priority: Pops node with minimum cost. Used in [[Best First Search - Graph]]
2. FIFO: Used in [[Breadth First Search]]
3. LIFO: Stack, pops the most recent node, used in [[Depth First Search]] 
