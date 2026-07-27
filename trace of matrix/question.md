# Maximum Trace

You are given an `N × N` matrix `A` consisting of positive integers.

The **trace** of a square matrix is defined as the sum of the elements on its main diagonal.

Your task is to find the maximum possible trace among all square submatrices of the given matrix.

## Input Format

- The first line contains a single integer `T`, the number of test cases.
- For each test case:
  - The first line contains an integer `N`.
  - The next `N` lines each contain `N` space-separated integers describing the matrix.

## Output Format

For each test case, print a single integer — the maximum trace among all square submatrices.

## Constraints

```text
1 ≤ T ≤ 100
1 ≤ N ≤ 500
1 ≤ A[i][j] ≤ 10^5
```

## Sample Input

```text
1
3
1 2 3
4 5 6
7 8 9
```

## Sample Output

```text
15
```

## Explanation

The maximum trace is obtained from the entire matrix:

```text
1 + 5 + 9 = 15
```

Since all matrix elements are positive, the optimal submatrix always starts from either the first row or the first column. :contentReference[oaicite:0]{index=0}
