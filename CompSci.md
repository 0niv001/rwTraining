---
sticker: lucide//code-2
---
[[Recursion]]



# Data
- Data can be stored in different formats, with various encodings e.g. ASCII, UCS, UTF-8. 
- Data is often created for 3 reasons: Backup, Input and Consumption. 

**Types of data:
- [[Structured data]]
- [[Unstructured data]]
- [[Semi-structured data]]

**Types of databases:
- [[Relational database]]
- [[Document oriented database]]
- [[Object oriented database]]

**Data Manipulation** - Shaping the data to answer question. 
- *Hierarchical indexing:
	- Grouping data into parents and child groups. 
	- Partial indexing allows to select subsets of data. 
- *Merging datasets:*  Allows us to find useful patterns.
- *Pivoting*: Reshaping data to examine from different perspectives. 

**Data Cleaning** - Choose which parts of the data are relevant. 
- *Remove missing and duplicates:* Analyse missing data to find collection problems. 
- *Replace values:* Fill values with NaN or 0 (constants) to avoid errors and bugs. 
- *Rename axis:* Use map and rename. 
- *Remove outliers*: Make use of array operations. 

**Data analysis:**
- Split data into groups
- Apply calculations
- Combine results. 
# AI / ML

#### Logic

**Types of logic**:
- [[First Order Logic]]
- [[Propositional Logic]]
#### Search algorithms
- Series of paths and actions that the algorithm is trying out. 
- Starting from the initial state new paths are created by extending existing ones. 
- Uses: Route finding, [[Routing]]problems, and DNA sequencing. 

**Types of Search Algorithms:**
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

We can compare these search algorithms by using [[Tech/Backlinks/CompSci/ADS/Asymptotic Notation]] and working out the worst case scenario. 

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
1. Priority: Pops node with minimum cost. Used in [[Best First Search - Graph]].
2. FIFO: Used in [[Breadth First Search]]
3. LIFO: Stack, pops the most recent node, used in [[Depth First Search]] 
#### Learning
**Types of learning**
1. [[Supervised Learning]]
2. [[Unsupervised Learning]]
3. [[Reinforcement Learning]]

**Performance Metrics:**
- [[Accuracy]]
- [[Precision & Recall]]
- [[ROC & AUC]]
- [[True+ & False-]]