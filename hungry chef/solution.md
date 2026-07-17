## Observations

- Buying all `N` burgers as normal costs `N × X`, which is the minimum possible cost.
- If `N × X > R`, then Chef cannot afford `N` burgers, so the answer is `-1`.
- Start by assuming all burgers are normal.
- Replacing one normal burger with one premium burger increases the total cost by `Y - X`.
- After buying all burgers as normal, the remaining money is:
  ```text
  extra = R - (N × X)
  ```
- The maximum number of premium burgers that can be bought is:
  ```text
  extra // (Y - X)
  ```
  but it cannot exceed `N`.
- The remaining burgers are normal burgers.
- Key Insight: Begin with the cheapest valid purchase (all normal burgers) and greedily upgrade as many burgers as possible to premium using the remaining budget.
```python
# cook your dish here greedy

for _ in range(int(input())):
    x,y,n,r=map(int,input().split())
    diff=y-x
    
    premium=0;normal=0
    
    if n*x >r:
        print(-1)
        continue
    
    extra=r-(n*x)
    premium=min(n,extra//diff)
    normal=n-premium
    
    print(normal,premium)
    
    
```
