## Observations

- The required pattern is:
  ```text
  A1 ≤ A2 ≥ A3 ≤ A4 ≥ A5 ...
  ```
- Traverse the array once from left to right and consider each adjacent pair.
- For every index:
  - If the index is even (0-based), we need:
    ```text
    A[i] ≤ A[i+1]
    ```
    If this condition is violated, swap the two elements.
  - If the index is odd (0-based), we need:
    ```text
    A[i] ≥ A[i+1]
    ```
    If this condition is violated, swap the two elements.
- A single left-to-right pass is sufficient because each swap fixes the current inequality without breaking the inequalities that have already been established. :contentReference[oaicite:1]{index=1}
- This achieves the required arrangement in linear time without sorting.
- Key Insight: Greedily fix each adjacent pair while scanning the array once. Whenever the required inequality is violated, swapping the two elements immediately restores the alternating "up-down" pattern and preserves all previously fixed positions. 
```python
# cook your dish here

for _ in range(int(input())):
    n=int(input())
    arr=list(map(int,input().split()))
    
    for i in range(n-1):
        if i % 2==0 and arr[i] > arr[i+1]: #even failed
            arr[i],arr[i+1]=arr[i+1],arr[i]
        elif i % 2!=0 and arr[i] < arr[i+1]: #odd failed
            arr[i],arr[i+1]=arr[i+1],arr[i]
        
    print(*arr)
```
https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/ANUUND
