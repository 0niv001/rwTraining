- Size of the tree is = to the # of nodes
- Depth is # of edges below the root node
- Height = # of edges above furthest leaf node
- In binary trees nodes can only have up to 2 children.
- A root has no parents, the depth of a node counts from the root and the height of a node counts towards the leaf.
- A nearly complete binary tree requires the nodes to fill in each level from left to right before starting the next level.



Traversal- going through the nodes
- Inorder
    - left > root > right
    - Go left first and then right
- Post order
    - Left > right > root
    - Leaf to root
- Pre order
    - root > left > right
    - Used for copying trees


## [[Binary Search]] trees

- Effective way to print has table values in sorted order with running time of O(n).
- Root needs to be > than left child and < than right child.
- The left most and right most are the smallest and biggest value respectively.
- A balanced BST guarantees O(lgn) time.
- Can be used as a dictionary and a PQ
- Basic operations take time proportional to the height of the tree
- O(lgn) in the worst case scenario for complete binary trees
- If the tree is a linear chain of nodes it will take O(n)
- Can be represented by a linked data structure where each node is object
- In addition to key and satellite each node has the attributes _left, right, and p_ → left child, right child, parent.
- Keys are stored in a way to satisfy binary search tree property.
- We can print all the keys in a BST in sorted order through a recursive algorithm called inorder tree walk

Red Black Trees

- Search tree schemes that are balanced so that the dynamic set operations take O(lgn) time in the worst case.

Properties

- Every node is red or black
- The root is black
- All simple paths from node to descendant have the same number of black nodes

- Internal nodes tend to have the key values
- The number of black nodes in a simple path from node x down to a leaf is the black heigh of the node bh(x)

Rotations
- Insert and Delete take O(lgn) time.
- When they change the tree we need to restore its properties.
- We change the pointer structure through rotation either left or right
- When we rotate to the left on a node x we assume right child is not nil
- Left rotation pivots around the link from x to y
- Both left and right rotate run in O(1) time.