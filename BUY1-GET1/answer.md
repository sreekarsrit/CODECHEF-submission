## Observations

- The Buy1-Get1 offer applies **independently for each jewel color**.
- Jewels of different colors cannot be paired together.
- For a color appearing `f` times:
  - Every pair of jewels requires paying for only one jewel.
  - Therefore, the minimum cost for that color is:
    ```text
    ceil(f / 2)
    ```
- This can be computed as:
  - `f // 2` if `f` is even.
  - `(f // 2) + 1` if `f` is odd.
- Count the frequency of every character in the string, compute the minimum cost for each color separately, and sum the costs.
- Key Insight: Treat each color independently and pay for only half of its occurrences (rounded up), since every purchased jewel can provide one free jewel of the same color.

```python
# cook your dish here

from collections import Counter
for _ in range(int(input())):

    s = Counter(input().strip())
    ans = 0
    # print(type(s))
    for i in s.values():
        if i%2==0:
            ans += i//2 
        else:
            ans += (i//2)+1
    print(ans)
    
```

This string represents whether each person successfully withdrew money (`1`) or not (`0`), exactly as required by the problem.
