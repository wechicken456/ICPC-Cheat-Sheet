
# ICPC reference

# Matrices
## Linear recurrences using matrix
k = how many coefficients are there in the recurrence formula.  
In the first k − 1 rows, each element is 0 except that one element is 1. These rows (with the element 1) replace f(i) with f(i+1), f(i+1) with f(i+2), and up to f(i + k -1).  
The last row contains the coefficients of the recurrence to calculate the new value f (i + k).

If V = adjacency matrix of an **unweighted** graph, then (V^n)[i][j] contains the numbers of paths of n edges between the i and j in the graph. (can repeat nodes and edges).

For a weighted graph, calculate for each pair of nodes the **minimum** length of a path between them that contains **exactly** n edges:
<img width="374" alt="image" src="https://user-images.githubusercontent.com/55309735/219503731-9c909295-2dcd-4234-b26a-2446a6ba7567.png">
(with B = A)

## Calculate the number of spanning trees using determinant of an adjacency matrix
Construct a matrix L where L[i][i] is the degree of node i, L[i][j] = −1 if there is an edge between nodes i and j, otherwise L[i][j] = 0. Then its determinant is the number of spanning trees.

# Strings
## Prefix function
https://cp-algorithms.com/string/prefix-function.html#efficient-algorithm
For the 2nd case of the 2nd optimization, we can move by setting `j = pi[j - 1]` because in the answer for `pi[j-1]`, its suffix will also be a suffix of `pi[j]`. 

If this is still not clear: f we want the next longest suffix of length j < pi[i], then `s[0..j]  = s[i - pi[i] + 1... i - pi[i] + j]`, but since by definition of `pi[i]`, we also have `s[0...k] == s[i - pi[i] + 1...i - pi[i] + k]` for k < j < pi[i]. So if `s[0...j]` to appears another time (in `s[i - pi[i] + 1... i]`) after the initial occurence at `i - pi[i] + 1`, then it would also have appeared earlier in `s[0...pi[i] - 1]`. That's why we can take steps of `j = pi[j - 1]`.
