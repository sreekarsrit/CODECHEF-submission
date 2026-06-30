# TCS Examination

Two friends, Dragon and Sloth, are writing a computer science examination series. There are three subjects in this series: `DSA`, `TOC`, and `DM`. Each subject carries `100` marks.

You know the individual scores of both Dragon and Sloth in all `3` subjects. You have to determine who got a better rank.

The rank is decided as follows:

1. The person with a bigger total score gets a better rank.
2. If the total scores are tied, the person who scored higher in `DSA` gets a better rank.
3. If the total score and the `DSA` score are tied, the person who scored higher in `TOC` gets a better rank.
4. If everything is tied, they get the same rank.

## Input Format

The first line of input contains a single integer `T`, denoting the number of test cases. The description of `T` test cases follows.

The first line of each test case contains three space-separated integers denoting the scores of Dragon in `DSA`, `TOC` and `DM` respectively.

The second line of each test case contains three space-separated integers denoting the scores of Sloth in `DSA`, `TOC` and `DM` respectively.

## Output Format

For each test case:

- Output `"Dragon"` if Dragon got a better rank.
- Output `"Sloth"` if Sloth got a better rank.
- Output `"Tie"` if they have the same rank.

The output is case insensitive.

## Constraints

```text
1 ≤ T ≤ 1000
0 ≤ Score ≤ 100
```

## Sample Input

```text
4
10 20 30
30 20 10
5 23 87
5 23 87
0 15 100
100 5 5
50 50 50
50 49 51
```

## Sample Output

```text
SLOTH
TIE
DRAGON
DRAGON
```

## Explanation

For the first test case, Sloth and Dragon have the same total score but Sloth gets a better rank because he has a higher score in `DSA`.

For the second test case, Sloth and Dragon have the same rank because they have the same score among all subjects.

For the third test case, Dragon gets a better rank because he has a greater total score.

For the fourth test case, Sloth and Dragon have the same total score and same `DSA` score. Dragon gets a better rank because he has a greater `TOC` score.
