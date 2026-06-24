# Farmer Feb

## Problem Statement

Farmer Feb has three fields with potatoes planted in them. He harvested `x` potatoes from the first field, `y` potatoes from the second field and is yet to harvest potatoes from the third field.

Feb is very superstitious and believes that if the total number of potatoes harvested from all three fields is a **prime number**, he will make a huge profit.

Your task is to determine the **minimum number of potatoes** that must be harvested from the third field so that:

```text
x + y + harvested_potatoes
```

becomes a prime number.

> **Note:** At least one potato must be harvested from the third field.

---

## Input Format

- The first line contains an integer `T`, the number of test cases.
- Each of the next `T` lines contains two integers:
  - `x` — potatoes harvested from the first field.
  - `y` — potatoes harvested from the second field.

---

## Output Format

For each test case, print a single integer denoting the minimum number of potatoes that need to be harvested from the third field to make the total count prime.

---

## Constraints

```text
1 ≤ T ≤ 1000
1 ≤ x ≤ 1000
1 ≤ y ≤ 1000
```

---

## Sample Input

```text
2
1 3
4 3
```

## Sample Output

```text
1
4
```

---

## Explanation

### Test Case 1

Current harvested potatoes:

```text
1 + 3 = 4
```

If Farmer Feb harvests `1` more potato:

```text
4 + 1 = 5
```

Since `5` is prime, the answer is:

```text
1
```

### Test Case 2

Current harvested potatoes:

```text
4 + 3 = 7
```

Checking values:

```text
7 + 1 = 8  (Not Prime)
7 + 2 = 9  (Not Prime)
7 + 3 = 10 (Not Prime)
7 + 4 = 11 (Prime)
```

Therefore, the minimum number of additional potatoes required is:

```text
4
```
