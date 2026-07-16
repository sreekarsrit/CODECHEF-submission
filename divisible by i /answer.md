## Observations

- We need to construct a **permutation**, so every number from `1` to `N` must appear exactly once.
- The condition applies only to **adjacent elements**:
  ```text
  i divides |P[i+1] - P[i]|
  ```
  for every `1 ≤ i ≤ N-1`.
- Since the problem guarantees that at least one valid permutation always exists, the task is to construct any such arrangement.
- The pattern used in the solution alternates between placing the largest remaining and the smallest remaining values, and finally reverses the sequence.
- This arrangement ensures that the absolute difference between consecutive elements satisfies the required divisibility condition for every index.
- Key Insight: Instead of checking divisibility while constructing the permutation, a carefully designed construction pattern automatically satisfies all the required conditions.
