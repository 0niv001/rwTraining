Running time of [[Search Algorithms]] or [[Algorithms]] depend on how long it takes a cpu to run the lines of code, specifically the primitive operations executed. 

To work out running time without influence of other factors, we look at the algorithms rate of growth. 

There are 3 main forms of asymptotic notation:
1. Big O notation- upper bound
2. Big-θ (Theta) notation- tight bound
3. Big Ω (Omega) notation- lower bound

Big O notation is usually used, as it gives the worst case scenario. 
## Functions in asymptotic notation
- If the algorithm takes a constant amount of time regardless of input size we use 1
- if it takes $log_n$ time, we use $log2$ as standard pracice. 
## Growth rate 
| Big-O   | Informal Name     |
| ------- | ----------------- |
| O(1)    | Constant          |
| O(lgn)  | Logarithmic       |
| O(n)    | Linear            |
| O(nlgn) | nlgn              |
| O(n^2)  | quadratic         |
| O(n^3)  | cubic             |
| O(2^n)  | Don't even bother |
