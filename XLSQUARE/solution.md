## Observations

- Each small square has side length `A`.
- To form a larger square without gaps or overlaps, the number of small squares used must itself be a perfect square.
- If `k × k` small squares are used, the side length of the mega square becomes:
  
  ```text
  k × A
  ```
- Therefore, we need the largest perfect square that does not exceed `N`.
- The largest integer `k` satisfying `k² ≤ N` is:
  
  ```text
  ⌊√N⌋
  ```
- From the sample:
  - `N = 5` → largest perfect square ≤ 5 is `4 = 2²` → side length = `2 × A`.
  - `N = 11` → largest perfect square ≤ 11 is `9 = 3²` → side length = `3 × A`.
- Key Insight: Find `⌊√N⌋` and multiply it by `A`.
```python
# cook your dish here
for _ in range(int(input())):
    n,a=map(int,input().split())
    print(a*int(n**0.5))
```
## Code Implementation Explanation

The solution first computes the integer part of the square root of `N`:

```python
int(n ** 0.5)
```

This gives the largest integer `k` such that:

```text
k² ≤ N
```

which means `k × k` is the maximum number of small squares that can be arranged to form a perfect square.

Since each small square has side length `A`, arranging `k` squares along each side produces a mega square with side length:

```python
a * int(n ** 0.5)
```

The code directly computes this value and prints it as the answer for each test case.
