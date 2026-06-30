## Observations

- The operation only reverses a substring that contains an equal number of `0`s and `1`s.
- Reversing such balanced substrings allows the `0`s and `1`s to be rearranged without changing their overall counts.
- The number of `0`s and `1`s in the string always remains the same after every operation.
- To obtain the lexicographically smallest binary string, all `0`s should appear before all `1`s.
- Therefore, the desired final arrangement is simply:
  
  ```text
  000...00111...11
  ```

  where the number of `0`s and `1`s remains unchanged.
- From the sample:
  - `01100` can be transformed into `00011`.
  - `0000` is already the smallest possible arrangement.
- Key Insight: Since only the frequencies of `0`s and `1`s matter, arranging all `0`s before all `1`s produces the lexicographically smallest string.
```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    arr=list(input())
    arr.sort()
    print("".join(arr))
```
## Code Implementation Explanation

The solution first converts the input string into a list of characters:

```python
arr = list(input())
```

The list is then sorted:

```python
arr.sort()
```

Since the string contains only binary characters, sorting places all `'0'` characters before all `'1'` characters.

Finally, the sorted characters are joined back into a single string:

```python
print("".join(arr))
```

This produces the lexicographically smallest possible binary string while preserving the original number of `0`s and `1`s.
