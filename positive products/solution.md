## Observations

- The product of two numbers is positive only if both numbers have the same sign.
- Two positive numbers always produce a positive product.
- Two negative numbers also produce a positive product.
- Any pair containing `0` can never have a product greater than `0`, so zeros are ignored.
- If there are `P` positive numbers, the number of valid positive-positive pairs is:
  ```text
  P × (P - 1) / 2
  ```
- If there are `N` negative numbers, the number of valid negative-negative pairs is:
  ```text
  N × (N - 1) / 2
  ```
- Key Insight: The final answer is the sum of the combinations of positive numbers and negative numbers taken two at a time.
```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    A=list(map(int,input().split()))
    
    pos=len([x for x in A if x>0])
    neg=len([x for x in A if x<0])
    
    print((pos*(pos-1)//2)+(neg*(neg-1)//2)) # n! is n*(n-1)/2 
```
