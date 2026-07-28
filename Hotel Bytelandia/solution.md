## Observations

- Treat every arrival and departure as an **event**.
- A guest is present during the interval:
  ```text
  [arrival, departure)
  ```
  so if an arrival time equals a departure time, the departure must be processed first.
- Sort the arrival times and departure times separately.
- Use two pointers:
  - One for the next arrival.
  - One for the next departure.
- While traversing:
  - If the next arrival time is **less than** the next departure time, an arrival occurs first, so increase the current guest count.
  - Otherwise, process the departure first and decrease the current guest count.
- After every arrival or departure event, update the maximum number of guests seen so far.
- Key Insight: Instead of checking every time instant, process the arrival and departure events in chronological order using two sorted arrays. This computes the maximum number of simultaneous guests in `O(N log N)` time.
```python
# cook your dish here
# t=int(input())

for _ in range(int(input())):
    n=int(input())
    
    cnt=0
    arr=list(map(int,input().split()))
    dep=list(map(int,input().split()))
    
    arr.sort()
    dep.sort()
    i=0;j=0
    maxGuest=0;currentGuest=0
    while i<n and j<n:
        
        if arr[i]<dep[j]:   #arriving event
            currentGuest +=1
            i+=1
        else:               #departure event
            currentGuest -=1
            j+=1
        
        if currentGuest>maxGuest:
            maxGuest=currentGuest
            
    print(maxGuest)
```
https://www.codechef.com/practice/course/2-star-difficulty-problems/DIFF1500/problems/HOTEL?tab=statement
