## Observations
### https://www.codechef.com/viewsolution/1308893247
- The frequency of every element needs to be counted.
- The element with the highest frequency is the required answer.
- If multiple elements have the same maximum frequency, the smallest element among them should be selected.
- A frequency dictionary (hash map) efficiently stores the occurrence count of each element.
- After computing all frequencies:
  - Find the maximum frequency.
  - Among all elements having this frequency, choose the minimum value.
- Key Insight: The problem reduces to counting frequencies first, then applying the tie-breaking rule of selecting the smallest element among those with the maximum frequency.
```python
def mostFrequent(N: int, A: list) -> list:
    freq={}
    
    for i in A:
        freq[i]=freq.get(i,0)+1
    max_freq=max(freq.values())
    rep_num=min(k for k in freq if freq[k]==max_freq)
    
    print(rep_num,max_freq)
    
for _ in range(int(input())):
    N=int(input())
    A=list(map(int,input().split()))
    mostFrequent(N,A)
```
