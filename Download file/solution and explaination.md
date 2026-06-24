## Observations

- The first `K` minutes of internet usage are completely free, regardless of the data usage rate.
- Internet usage is divided into `N` consecutive segments.
- For a segment with duration `Ti` and usage rate `Di`, the total data consumed is `Ti × Di`.
- The free minutes may:
  - cover an entire segment,
  - partially cover a segment,
  - or be exhausted before reaching a segment.
- Only the minutes not covered by the free quota contribute to the final bill.
- From the sample:
  - If the free minutes completely cover the first segment, charging starts from the next segment.
  - If the free minutes end in the middle of a segment, only the remaining part is charged.
  - If `K = 0`, every minute is charged.
- Key Insight: For each segment, use as many free minutes as possible first and charge only for the remaining minutes.

```python
# cook your dish here
for _ in range(int(input())):
    n,k=map(int,input().split())
    price=0
    for _ in range(n):
        t,d=map(int,input().split())
        
        free=min(t,k)
        paid=t-free
        
        price+=paid*d
        k=k-free
        
    print(price)
    
```

## Code Implementation Explanation

The variable `k` stores the number of free minutes that are still available.

For every usage segment, the code first calculates how many minutes can be covered by the remaining free quota:

```python
free = min(t, k)
```

If the segment duration is smaller than the remaining free minutes, the entire segment becomes free. Otherwise, only part of the segment is free.

The number of chargeable minutes in the current segment is:

```python
paid = t - free
```

Since the usage rate is `d` MB per minute and the provider charges `$1` per MB, the cost contributed by this segment is:

```python
price += paid * d
```

After consuming some free minutes, the remaining free quota is updated:

```python
k = k - free
```

By processing every segment in order, the code ensures that the first `K` minutes are free and charges only for the remaining usage, producing the final amount Chef has to pay.
