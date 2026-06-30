## Observations

- Each win gives `2` points, a tie gives `1` point, and a loss gives `0` points.
- Since we need to minimize the number of wins, it is always better to replace a required win with ties whenever possible.
- Every tie can cover `1` required point without increasing the win count.
- At most `Y` points can be earned using only ties.
- If `X ≤ Y`, RCB can qualify using only ties, so no wins are required.
- If `X > Y`, after taking all possible ties, the remaining points must come from wins.
- The remaining points required are:
  
  ```text
  X - Y
  ```

- Each win contributes one additional point compared to a tie (`2` instead of `1`), so the minimum number of wins equals the remaining required points.
- Key Insight: The minimum number of wins is `max(X - Y, 0)`.
##solution
```python
# cook your dish here
for _ in range(int(input())):
    x, y = map(int,input().split()) 
    print(max(x-y,0))
```
## Code Implementation Explanation

The solution computes the difference between the required points and the maximum points that can be obtained using only ties:

```python
x - y
```

If `X` is less than or equal to `Y`, RCB can qualify by drawing matches, so no wins are needed.

Otherwise, the remaining points must come from wins.

The code directly computes this using:

```python
max(x - y, 0)
```

If `x - y` is negative, it means ties are sufficient, so the answer is `0`.

Otherwise, `x - y` gives the minimum number of matches that RCB must win, which is printed as the final answer.
