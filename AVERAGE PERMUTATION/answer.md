## Observations

- Every element contributes to one or more consecutive triplets.
- Middle elements participate in more triplets than the elements near the ends.
- To minimize the total sum, larger values should appear in positions that contribute to fewer triplets whenever possible.
- The problem guarantees that multiple optimal permutations may exist, so any valid construction achieving the minimum is acceptable.
- The implemented construction places:
  - `N` and `N-2` at the beginning,
  - the smallest values in increasing order through the middle,
  - and finally `N-3` and `N-1` at the end.
- For the special case `N = 3`, every permutation gives the same sum, so any permutation is valid.
- Key Insight: Arrange the largest numbers near the ends of the permutation and keep the smaller numbers in the positions that appear in more consecutive triplets, thereby minimizing the overall sum of triplet averages.
```python
for _ in range(int(input())):
    n=int(input())
    
    if n==3:
        print(1,2,3)
    else:
        ans=[n,n-2]
        
        for i in range(1,n-3):
            ans.append(i)
        
        ans.extend([n-3,n-1])
        print(*ans)
```
