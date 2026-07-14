# Positive Products
## https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/POSPROD?tab=statement
You are given an array `A` of length `N`.

Find the number of pairs of indices `(i, j)` such that:

- `1 ≤ i < j ≤ N`
- `Aᵢ · Aⱼ > 0`

## Input Format

- The first line contains a single integer `T` - the number of test cases.
- The first line of each test case contains an integer `N` - the size of the array `A`.
- The second line of each test case contains `N` space-separated integers `A₁, A₂, …, Aₙ` denoting the array `A`.

## Output Format

For each test case, output the number of pairs which satisfy the above conditions.

## Constraints

```text
1 ≤ T ≤ 1000
2 ≤ N ≤ 10^5
-10^4 ≤ Ai ≤ 10^4

The sum of N over all test cases does not exceed 2 × 10^5.
```

## Sample Input

```text
3
5
1 -3 0 2 -1
4
-1 -1 -1 -1
4
0 1 2 3
```

## Sample Output

```text
2
6
3
```

## Explanation

**Test case 1:** The pairs which satisfy the conditions are `(1,4)` and `(2,5)`.

**Test case 2:** The pairs which satisfy the conditions are `(1,2)`, `(1,3)`, `(1,4)`, `(2,3)`, `(2,4)` and `(3,4)`.

**Test case 3:** The pairs which satisfy the conditions are `(2,3)`, `(2,4)` and `(3,4)`.
