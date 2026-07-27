## Observations

- The trace of a square matrix is the sum of the elements on its main diagonal.
- Since every element of the matrix is positive, extending a valid diagonal always increases its trace.
- Therefore, the maximum trace can only come from diagonals that start:
  - in the first row, or
  - in the first column.
- For every starting position in the first column:
  - Traverse diagonally down-right while accumulating the sum.
- Similarly, for every starting position in the first row:
  - Traverse diagonally down-right and compute its sum.
- Keep track of the maximum diagonal sum among all these traversals.
- The main diagonal is included when starting from `(0, 0)`, so although it is visited twice in the straightforward implementation, this does not affect the final maximum.
- Key Insight: Because all entries are positive, it is sufficient to evaluate only the diagonals beginning in the first row or first column instead of considering every possible square submatrix, reducing the solution to an `O(N²)` traversal. 2]{index=2}
```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    mat=[]
    ans=float('-INF')
    for _ in range(n):
        line=list(map(int,input().split()))
        mat.append(line)
    
    for i in range(n):
        x=i;y=0
        leftmax=0
        rightmax=0
        while x<n and y<n:
            leftmax+=mat[x][y]
            rightmax+=mat[y][x]
            x+=1;y+=1
        ans=max(ans,leftmax,rightmax)
    print(ans)
```
https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/TRACE?tab=statement
