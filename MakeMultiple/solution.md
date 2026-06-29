## Observations

- The same value `X` is added to both `A` and `B`.
- Therefore, the difference between the two numbers never changes:
  
  ```text
  (B + X) - (A + X) = B - A
  ```
- Let `diff = B - A`.
- After adding `X`, suppose `(B + X)` becomes a multiple of `(A + X)`:

  ```text
  B + X = k × (A + X)
  ```

- Rearranging,

  ```text
  diff = (k - 1) × (A + X)
  ```

- This means `(A + X)` must divide `diff`.
- If `B` is already divisible by `A`, then choosing `X = 0` immediately satisfies the condition.
- Otherwise, we need a divisor of `diff` that is at least `A`, since `A + X ≥ A`.
- Such a divisor exists only when:

  ```text
  diff ≥ A
  ```

- From the sample:
  - `(3,6)` → already divisible → `YES`.
  - `(4,14)` → `diff = 10 ≥ 4`, choose `X = 1` → `5 | 15`.
  - `(9,10)` → `diff = 1 < 9` → impossible.
- Key Insight: The answer is `YES` if `B` is already divisible by `A`, or if `B - A ≥ A`; otherwise, it is `NO`.
```python
# cook your dish here
for _ in range(int(input())):
    a,b=map(int,input().split())
    
    diff =b-a
    
    
    if b%a==0:
        print("YES")
    else:
        if a<=diff:
            print("YES")
        else:
            print("NO")
```

## Code Implementation Explanation

The solution first computes the difference between the two numbers:

```python
diff = b - a
```

This difference remains unchanged even after adding the same value `X` to both numbers.

The code first checks whether `B` is already divisible by `A`:

```python
if b % a == 0:
    print("YES")
```

If this condition is true, choosing `X = 0` is sufficient.

Otherwise, the code checks:

```python
if a <= diff:
    print("YES")
```

If the difference is at least `A`, it is possible to choose a suitable value of `X` so that `(A + X)` becomes a divisor of `(B + X)`.

If neither condition is satisfied, no valid value of `X` exists, and the code prints:

```python
print("NO")
```

Thus, the solution relies on checking the current divisibility and the relationship between `A` and the constant difference `B - A`.
