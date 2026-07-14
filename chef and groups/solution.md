## Observations

- A group consists of one or more consecutive `'1'`s.
- Every maximal continuous block of `'1'`s represents exactly one group.
- Consecutive `'1'`s belong to the same group and should not be counted multiple times.
- A new group starts only when:
  - The current character is `'1'`, and
  - The previous seat is either `'0'` or does not exist (beginning of the string).
- `'0'`s act as separators between different groups.
- If the string contains only `'0'`s, there are no groups.
- Key Insight: Count the number of times a `'1'` appears immediately after a `'0'` (or at the beginning of the string). Each such occurrence represents a new group.
```python
# cook your dish here
n=int(input())
for _ in range(n):
    s=input()
    group=0
    seatEmpty=1
    for i in s:
        if i=='1' and seatEmpty==1:
            group+=1
            seatEmpty=0
        elif i=='0':
            seatEmpty=1
    print(group)
```
