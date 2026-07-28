# Hotel Bytelandia

A hotel has `N` guests. For each guest, you are given:

- their arrival time, and
- their departure time.

A guest stays in the hotel from the arrival time **inclusive** to the departure time **exclusive**. That is, if a guest departs at time `t`, they are **not** present in the hotel at time `t`.

Find the maximum number of guests that are present in the hotel at the same time.

## Input Format

- The first line contains an integer `T`, the number of test cases.
- For each test case:
  - The first line contains an integer `N`.
  - The second line contains `N` integers denoting the arrival times.
  - The third line contains `N` integers denoting the departure times.

## Output Format

For each test case, print a single integer — the maximum number of guests present in the hotel simultaneously.

## Constraints

```text
1 ≤ T ≤ 100
1 ≤ N ≤ 100
1 ≤ Arrivali < Departurei ≤ 1000
```

## Sample Input

```text
3
3
1 2 3
2 3 4
4
1 2 10 5
4 5 12 9
2
1 2
2 3
```

## Sample Output

```text
1
2
1
```

## Explanation

A guest is considered to be in the hotel during the interval `[arrival, departure)`. Therefore, when an arrival time and a departure time are equal, the departure is processed first, and the arriving guest is counted only afterwards. 
