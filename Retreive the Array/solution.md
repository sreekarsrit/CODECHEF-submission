## Observations

- Let the sum of all elements in the original array be:
  ```text
  SUM = A1 + A2 + ... + AN
  ```
- Since
  ```text
  Bi = prefi + suffi
  ```
  expanding both sums gives:
  ```text
  Bi = SUM + Ai
  ```
- Therefore, every element of `B` is simply the total sum of `A` plus the corresponding element of `A`.
- Summing all elements of `B`:
  ```text
  B1 + B2 + ... + BN
  = (N + 1) × SUM
  ```
- Hence,
  ```text
  SUM = (sum of B) / (N + 1)
  ```
- Once `SUM` is known, every element of the original array is:
  ```text
  Ai = Bi - SUM
  ```
- Key Insight: Recover the total sum of the original array from the sum of `B`, then subtract it from each `Bi` to obtain the corresponding `Ai`. :contentReference[oaicite:1]{index=1}

```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    B=list(map(int,input().split()))
    
    A=[]
    B_sum=sum(B)
    tot=int(B_sum/(n+1))
    
    for i in range(n):
        ans=B[i]-tot
        A.append(ans)
    print(*A)
```
https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/ARRAYRET
