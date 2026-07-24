# Retrieve the Array

Chef has an array `A` of length `N`.

Let

```text
prefi = A1 + A2 + ... + Ai
suffi = Ai + Ai+1 + ... + AN
```

Now Chef created another array `B` of length `N` such that

```text
Bi = prefi + suffi
```

Chef lost the original array `A` and wants to recover it with the help of `B`. Help Chef to recover the array.

It is guaranteed in the input that there exists a valid array `A` for the given array `B`. In case of multiple valid arrays `A`, output any valid array.

## Input Format

- The first line of input contains a single integer `T`, denoting the number of test cases.
- The first line of each test case contains an integer `N`.
- The second line contains `N` space-separated integers `B1, B2, ..., BN`.

## Output Format

For each test case, output `N` space-separated integers denoting the recovered array `A`.

## Constraints

```text
1 ≤ T ≤ 10^5
1 ≤ N ≤ 10^5
1 ≤ Ai ≤ 10^5

The sum of N over all test cases does not exceed 10^5.
```

## Sample Input

```text
2
3
7 8 9
4
13 11 12 10
```

## Sample Output

```text
1 2 3
3 1 2 0
```

## Explanation

For every index,

```text
Bi = prefi + suffi
```

Using the given array `B`, the original array `A` can be uniquely reconstructed. :contentReference[oaicite:0]{index=0}
