https://www.codechef.com/practice/course/1-star-difficulty-problems/DIFF1200/problems/HOSTELROOM?tab=statement
Hostel Room
There are initially 
�
X people in a room.

You are given an array 
�
A of length 
�
N which describes the following events:

If 
�
�
≥
0
A 
i
​
 ≥0, then 
�
�
A 
i
​
  people enter the room at 
�
i-th minute. For e.g. if 
�
2
=
3
A 
2
​
 =3, then 
3
3 people enter the room at the 
2
2-nd minute.
If 
�
�
<
0
A 
i
​
 <0, then 
∣
�
�
∣
∣A 
i
​
 ∣ people leave the room at 
�
i-th minute. Here 
∣
�
�
∣
∣A 
i
​
 ∣ denotes the absolute value of 
�
�
A 
i
​
 . For e.g. if 
�
4
=
−
2
A 
4
​
 =−2, then 
2
2 people leave the room at the 
4
4-th minute.
Determine the maximum number of people in the room at any moment of time.

It is guaranteed in the input that at any moment of time, the number of people in the room does not become negative.

Input Format
The first line will contain 
�
T - the number of test cases. Then the test cases follow.
The first line of each test case consists of two integers 
�
N and 
�
X - the length of the array 
�
A and the number of people in the room initially.
The second line of each test case contains 
�
N integers 
�
1
,
�
2
,
�
3
,
…
�
�
A 
1
​
 ,A 
2
​
 ,A 
3
​
 ,…A 
N
​
 .
Output Format
For each testcase, output the maximum number of people in the room at any point of time.
