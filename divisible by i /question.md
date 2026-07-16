# Divisible by i
##https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/DIVBYI?tab=Submissions
You are given an integer `N`.

Construct a permutation `P` of length `N` such that

- For all `i (1 ≤ i ≤ N−1)`, `i` divides `abs(Pᵢ₊₁ − Pᵢ)`.

Recall that a permutation of length `N` is an array where every integer from `1` to `N` occurs exactly once.

It can be proven that for the given constraints at least one such `P` always exists.

## Input Format

- The first line of input contains a single integer `T`, denoting the number of test cases.
- The only line of each test case contains an integer `N` - the length of the array to be constructed.

## Output Format

For each test case, output a single line containing `N` space-separated integers `P₁, P₂, …, Pₙ`, denoting the elements of the array `P`.

If there exist multiple such arrays, print any.

## Constraints

```text
1 ≤ T ≤ 5 × 10^4
2 ≤ N ≤ 10^5

The sum of N over all test cases does not exceed 10^5.
```

## Sample Input

```text
2
2
3
```

## Sample Output

```text
1 2
2 1 3
```

## Explanation

**Test case 1:** A possible array satisfying all the conditions is `[1,2]`:

- For `i = 1`:
  `abs(A₂ − A₁) = abs(2 − 1) = 1` is divisible by `1`.

**Test case 2:** A possible array satisfying all the conditions is `[2,1,3]`:

- For `i = 1`:
  `abs(A₂ − A₁) = abs(1 − 2) = 1` is divisible by `1`.

- For `i = 2`:
  `abs(A₃ − A₂) = abs(3 − 1) = 2` is divisible by `2`.
