## Observations

- Since the only allowed operation is **increasing** an element, no element can ever be decreased.
- Therefore, if after sorting an element is already greater than its target value (`i + 1`), it is impossible to obtain the required permutation.
- Sort the array so that the smallest elements are matched with the smallest required values (`1, 2, ..., N`).
- After sorting:
  - The `i`-th element should become `i + 1`.
  - If `A[i] > i + 1`, print `-1`.
  - Otherwise, increase `A[i]` to `i + 1`, requiring:
    ```text
    (i + 1) - A[i]
    ```
    operations.
- The minimum total operations is the sum of these increments over all elements.
- Key Insight: After sorting, greedily assign each element to the smallest possible unused value (`1` to `N`). If any element is already too large for its position, the permutation cannot be formed; otherwise, sum the required increments. 
```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    arr=list(map(int,input().split()))
    arr.sort()
    cnt=0
    possible=True
    
    for i in range(n):
        if arr[i]>i+1:
            possible=False
            break
        cnt+=(i+1)-arr[i]
            
    if possible:print(cnt)
    else:print(-1)
```
https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/PERMUTATION
