```python
# cook your dish here
for _ in range(int(input())):
    n,x=map(int,input().split())
    a=list(map(int,input().split()))
    curr_strength=max_strength = max(0,x)
    
    for i in a:
        curr_strength+=i
        if curr_strength>max_strength:
            max_strength=curr_strength
            
    print(max_strength)
```
