## Huffman Trees

- Running time of O(nlgn) since heap operations inside the loop take O(lgn).
- Works by extracting two elements of smallest frequency for min priority queue, making a new node that has the sum of the two frequencies and putting them together.
- Huffman tree is optimal since every time the node is used it is the one with the smallest frequency.
- Compresses data allowing us to save 20-90% of space.
- We consider the data to be a sequence of characters.

Prefix codes

[[Binary Trees]]

## Priority Q

- Application of a heap, comes in two forms: Max and Min PQ.
- Data structure for maintaining set S of elements each with a value called a key.
- Elements of PQ correspond to objects in the application

Max/Min PQ Operations

- Heap maximum uses the max operation in O(1) time
- Running time of heap extract max is O(lgn)
- Running time of Heap-increase-key and Max-heap-insert on and n element heap is O(lgn).

## Graphs

- Representing graphs is first step towards computational implementation
- There are two ways to represent graphs _G = (V,E_):
    - Collection of adjacency list.
    - Adjacency matrix.
- _G = (V,E_)- _V_ is vertex, and elements are called vertices ( represented by circles) _E_ is the edge
- Vertex with 0 degrees is isolated
- If (_u,v_) is an edge in a directed graph (_V,E_) we say that its incident from or leaves vertex u and is incident to and enters vertex c. In an undirected graph we say that (_u,v_) is incident on u,v.
- If (_u,v_) is an edge in a graph, we say that vertex _v_ is adjacent to vertex _u_, in undirected graphs the adjacency relation is symmetric, and in directed graphs it is not necessarily so.

Cycles

Paths

Directed

Undirected