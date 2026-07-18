## Observations

- The berth arrangement repeats after every block of `8` seats.
- Therefore, only the position of a seat within its block determines its train partner.
- Compute the seat's position inside the current block using `N % 8`.
  - If `N % 8 == 0`, the position is considered `8`.
- Find the starting seat number of the current block:
  ```text
  base = ((N - 1) // 8) × 8
  ```
- Each position has a fixed partner and berth type:

  | Position | Partner Position | Berth |
  |----------|------------------|-------|
  | 1 | 4 | LB |
  | 2 | 5 | MB |
  | 3 | 6 | UB |
  | 4 | 1 | LB |
  | 5 | 2 | MB |
  | 6 | 3 | UB |
  | 7 | 8 | SU |
  | 8 | 7 | SL |

- The final seat number is obtained by adding the partner position to the block's base.
- Key Insight: Since the seating pattern repeats every 8 berths, solve the problem by identifying the seat's position within its 8-seat block and mapping it to its fixed partner.
```python
# cook your dish here
for _ in range(int(input())):
    n=int(input())
    
    if n%8==0:
        rem=8
    else:
        rem=n%8
    
    base=((n-1)//8)*8
    
    match rem:
        case 1:
            seat, berth = base + 4, "LB"
        case 2:
            seat, berth = base + 5, "MB"
        case 3:
            seat, berth = base + 6, "UB"
        case 4:
            seat, berth = base + 1, "LB"
        case 5:
            seat, berth = base + 2, "MB"
        case 6:
            seat, berth = base + 3, "UB"
        case 7:
            seat, berth = base + 8, "SU"
        case 8:
            seat, berth = base + 7, "SL"
        
    print(f"{seat}{berth}")
```
