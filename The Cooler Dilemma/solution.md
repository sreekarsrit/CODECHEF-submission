## Observations

- Renting for `m` months costs:

  ```text
  m × X
  ```

- We need the maximum value of `m` such that:

  ```text
  m × X < Y
  ```

- This is a strict inequality, so renting cost cannot become equal to the purchase cost.
- The first value of `m` for which the renting cost becomes greater than or equal to `Y` is:

  ```text
  ⌈Y / X⌉
  ```

- Therefore, the maximum valid number of rental months is one less than this value:

  ```text
  ⌈Y / X⌉ - 1
  ```

- From the sample:
  - `X = 5`, `Y = 12` → `⌈12/5⌉ = 3` → Answer = `2`.
  - `X = 5`, `Y = 5` → `⌈5/5⌉ = 1` → Answer = `0`.
- Key Insight: Find the smallest number of months where renting is no longer cheaper than buying, then subtract one.
```python
# cook your dish here
import math
for _ in range(int(input())):
 x,y=map(int,input().split())
 print(math.ceil(y/x)-1)
```

## Code Implementation Explanation

The solution computes the ceiling of the division:

```python
math.ceil(y / x)
```

This gives the smallest number of months for which the renting cost becomes greater than or equal to the purchase cost.

Since the renting cost must be **strictly less** than the purchase cost, the maximum valid number of rental months is one less than this value.

The code directly computes:

```python
math.ceil(y / x) - 1
```

and prints the result for each test case.

This correctly handles all cases, including when renting even for one month is not cheaper than purchasing, in which case the answer becomes `0`.
