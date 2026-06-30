# End Sorted

Chef considers a permutation `P` of `{1,2,3,…,N}` **End Sorted** if and only if:

- `P₁ = 1`
- `Pₙ = N`

Chef is given a permutation `P`.

In one operation Chef can choose any index `i (1 ≤ i ≤ N−1)` and swap `Pᵢ` and `Pᵢ₊₁`.

Determine the minimum number of operations required by Chef to make the permutation `P` End Sorted.

> **Note:** An array `P` is said to be a permutation of `{1,2,3,…,N}` if `P` contains each element of `{1,2,3,…,N}` exactly once.

## Input Format

- The first line of input will contain a single integer `T`, denoting the number of test cases.
- Each test case consists of two lines of input.
- The first line of each test case contains a single integer `N`, denoting the length of the permutation `P`.
- The second line contains `N` space-separated integers `P₁, P₂, …, Pₙ`, denoting the permutation `P`.

## Output Format

For each test case, output the minimum number of operations required by Chef to make the permutation `P` End Sorted.

## Constraints

```text
1 ≤ T ≤ 1000
2 ≤ N ≤ 10^5

P is a permutation of {1,2,3,…,N}

The sum of N over all test cases does not exceed 3 × 10^5.
```

## Sample Input

```text
4
4
1 3 2 4
3
3 2 1
2
2 1
3
2 1 3
```

## Sample Output

```text
0
3
1
1
```

## Explanation

**Test case 1:** `P` is already End Sorted.

**Test case 2:** `P` can be made End Sorted using `3` operations as follows:

```text
[3,2,1] → [2,3,1] → [2,1,3] → [1,2,3]
```

It can be shown that achieving this in fewer than `3` moves is impossible.

**Test case 3:** `P` can be made End Sorted using one operation, by swapping `1` and `2`.

**Test case 4:** `P` can be made End Sorted using one operation, by swapping `1` and `2`.
