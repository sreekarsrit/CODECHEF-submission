https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/ANUUND

# Ups and Downs

Given an array `A` of `N` integers, rearrange the elements of the array such that:

- `A1 ≤ A2`
- `A2 ≥ A3`
- `A3 ≤ A4`
- `A4 ≥ A5`
- and so on.

More formally,

- `A[i] ≤ A[i+1]` if `i` is odd.
- `A[i] ≥ A[i+1]` if `i` is even.

If there are multiple possible arrangements, print any one of them.

## Input Format

- The first line contains an integer `T`, the number of test cases.
- For each test case:
  - The first line contains an integer `N`.
  - The second line contains `N` space-separated integers representing the array.

## Output Format

For each test case, output a single line containing `N` space-separated integers representing the rearranged array satisfying the required conditions.

## Constraints

```text
1 ≤ T ≤ 100
1 ≤ N ≤ 10^5
1 ≤ Ai ≤ 10^9

The sum of N over all test cases does not exceed 10^5.
```

## Sample Input

```text
2
4
4 3 5 1
5
4 3 5 1 2
```

## Sample Output

```text
3 5 1 4
3 5 1 4 2
```

Any valid arrangement satisfying the required inequalities is accepted. :contentReference[oaicite:0]{index=0}
