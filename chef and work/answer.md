## Observations

- Boxes must be picked in order from left to right because Chef cannot access a box until all previous boxes have been moved or picked in the current trip.
- Therefore, the order of boxes cannot be changed.
- If any single box has a weight greater than `K`, it is impossible to carry that box, so the answer is `-1`.
- Otherwise, while traversing the boxes from left to right:
  - Keep adding box weights to the current trip as long as the total weight does not exceed `K`.
  - As soon as adding the next box exceeds `K`, start a new trip with that box.
- Since the order is fixed, filling each trip with as many consecutive boxes as possible always minimizes the total number of trips.
- Key Insight: A greedy approach of maximizing the number of consecutive boxes carried in each trip produces the minimum number of round trips.
```python
# cook your dish here greedy approch
for _ in range(int(input())):
    n,limit=map(int,input().split())
    W=list(map(int,input().split()))
    
    if max(W)>limit:
        print(-1)
        continue
    
    trips=1
    cur=0
    for i in W:
        
        if cur+i<=limit:
            cur+=i
        else:
            trips+=1
            cur=i
        
    print(trips)
```
