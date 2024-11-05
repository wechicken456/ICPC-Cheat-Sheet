
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



# Team strategy
Standard variable names:
    + `s` for string
    + `l` for string lenth
    + `v` for vectors
    + `n` for vector size
    + `m` for maps
    + `i`->`j`->`k` for loop iters

DO NOT GO TO SONIC BEFORE YOU TO SLEEP AT NIGHT. HAVE A GOOD DIET. HAVE AT LEAST 8 HOURS OF SLEEP.

AT THE BEGINNING:
1. One person should code up a template. Others should start reading.
2. Don't be fooled - SHORTER DOES NOT MEAN EASIER.
3. IF there's a really easy problem, do it now. Let other people continue reading.
4. Finish reading all problems before 45 minutes.
5. If someone else is at the terminal, teammates should write their code on paper. Only important parts.
    + Come up with corner test cases. => 20-minute penalty if you get it wrong.

DURING THE CONTEST:
1. 1 typer, 2 thinkers. 
2. Use good judgement to decide if you need your teammate's help.
3. Write down some notes on what techniques you think this problem requires, in case your teammate wants to work on another problem they would have some direction.
4. Read the room. You can see which problems are being solved on the scoreboard.
5. Keep track of all submissions on a sheet of paper, and keep track of who is working on what problem.
6. Print early, print often. Print every time you submit.



SPECIALIZATION;
1. Noah: Graph. Geometry
2. Tin: Range Query, Math, Combinatorics, Strings.
3. Divyessh: Misc?



