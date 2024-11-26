- Halving approach when trying to select something.
- Efficient for finding item from a sorted list.
- Most commonly used to find items in big arrays.
- Main concept is to keep track of a range of guesses.
- Very efficient when compared to linear search.

Recursion (Repetition) aims to solve a problem by solving smaller instances of the same problem.

Base-2 Logarithm is a maths function that means the same thing as “the number of times we can repeatedly halve starting at n until we get a value 1 plus one”, written as: $log2n$ or $lgn$

The logarithm function grows slowly. They are the reverse of exponentials who grow incredibly rapidly.

The running time of an algo for a specific input depends on the number of operations executed. higher number of operations == higher runtime

**Steps**
1. Set counter to middle of list
2. If that is the value, search is over. 
3. If value at midpoint is less / more the other half is ignored 
4. Repeat until item is found, or there are no items left. 