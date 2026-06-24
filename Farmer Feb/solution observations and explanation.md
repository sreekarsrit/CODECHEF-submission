## Observations

- Let the number of potatoes harvested from the third field be `k`.
- The final harvested count becomes `x + y + k`.
- Farmer Feb wants this final sum to be a prime number.
- At least one potato must be harvested from the third field, so `k ≥ 1`.
- We need to find the smallest possible value of `k` such that `x + y + k` becomes prime.
- Since prime numbers occur frequently, we can keep checking consecutive values of `k` starting from `1` until we find a prime sum.
- From the sample:
  - `x + y = 4`, and `4 + 1 = 5` is prime, so the answer is `1`.
  - `x + y = 7`, and the next prime after `7` is `11`, requiring `4` additional potatoes.
- Key Insight: Find the first prime number greater than `x + y` and output the difference between that prime and `x + y`.
```python
# cook your dish here
def isprime(num):
    if num<2:
        return False
    for i in range(2,int(num**0.5)+1):
        if num%i==0:
            return False
            
    return True
        
        
for _ in range(int(input())):
    x,y=map(int,input().split())
    i=1
    while True:
        if isprime(x+y+i):
            print(i)
            break
        i+=1
```
## Code Implementation Explanation

The solution first defines an `isprime()` function to check whether a number is prime.

```python
def isprime(num):
```

The function checks divisibility from `2` up to `√num`. If any divisor exists, the number is not prime; otherwise, it is prime.

For each test case, the code starts with:

```python
i = 1
```

because at least one potato must be harvested from the third field.

It then repeatedly checks whether the new total:

```python
x + y + i
```

is prime.

```python
if isprime(x + y + i):
```

As soon as a prime sum is found, the current value of `i` is printed and the loop stops.

Since `i` is tested in increasing order starting from `1`, the first valid value found is guaranteed to be the minimum number of potatoes that must be harvested from the third field.
