# Average Permutation

You are given an integer `N`.

Find a permutation

```text
P = [P1, P2, …, PN]
```

of the integers

```text
{1, 2, …, N}
```

such that the sum of averages of all consecutive triplets is minimized, i.e.

```text
N-2
 Σ   (Pi + Pi+1 + Pi+2) / 3
i=1
```

is minimized.

If multiple permutations are possible, print any of them.

## Input Format

- The first line of input will contain a single integer `T`, denoting the number of test cases.
- The first and only line of each test case contains an integer `N`, the size of the permutation.

## Output Format

For each test case, output on a new line a permutation which satisfies the above conditions.

## Constraints

```text
1 ≤ T ≤ 1000
3 ≤ N ≤ 10^5

The sum of N over all test cases won't exceed 3 × 10^5.
```

## Sample Input

```text
2
4
3
```

## Sample Output

```text
3 2 1 4
3 2 1
```

## Explanation

**Test case 1:** The sum is

```text
(P1 + P2 + P3) / 3 + (P2 + P3 + P4) / 3
= (3 + 2 + 1) / 3 + (2 + 1 + 4) / 3
= 6 / 3 + 7 / 3
= 4.333...
```

Among all possible permutations of `{1, 2, 3, 4}`, this is one of the permutations which provides the minimum result.

**Test case 2:** The sum is

```text
(3 + 2 + 1) / 3 = 6 / 3 = 2
```

Every permutation of size `3` will have this value, hence it is the minimum possible.
