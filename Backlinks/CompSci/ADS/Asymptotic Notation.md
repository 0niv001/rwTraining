Running time of [[Algorithms]] depend on how long it takes a cpu to run the lines of code, specifically the primitive operations executed. 

To work out running time without influence of other factors, we look at the algorithms rate of growth. 

There are 3 main forms of asymptotic notation:
1. Big O notation- upper bound
2. Big-θ (Theta) notation- tight bound
3. Big Ω (Omega) notation- lower bound

Big O notation is usually used, as it gives the worst case scenario. 
## Functions in asymptotic notation
- If the algorithm takes a constant amount of time regardless of input size we use 1
- if it takes $log_n$ time, we use $log2$ as standard practice. 
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
## Big O Rules
- If algo performs f(N) steps, then its O(N)
- If algo performs f(N) steps, followed by g(N) steps -> O(f(N) + g(N)) -> O(2N)
- If f(N) > g(N) then O(f(N) + g(N)) -> O(f(N))
- O(C + f(N)) -> O(f(N))
- If algo performs g(N) steps for each of f(N) steps -> O(f(N) * g(N)) -> O(N^2)
- O(1) - 1 Action
- O(N) - 1 Action per input
- O(N^2) - For each input, loop through the inputs again - usually nested
- O(logN) - Divide search space into 2 pieces at each step. - trees
- O(2^N) - Selection of items. 
