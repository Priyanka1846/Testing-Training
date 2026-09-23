### 17/09/2029
## Test Case Document

Task Link - https://docs.google.com/spreadsheets/d/1RXd-QSDysk9iYf62sDZA2-BzGseUhxkbaIV3ppgLlEo/edit?gid=0#gid=0

### 18/09/2026
## Test Case Using Jira

Task Link- https://priyankasworkspace-34516593.atlassian.net/browse/T1-22

### 22/09/2026
## Equivalence Partition Test Case Exercises 

Task Link - https://docs.google.com/spreadsheets/d/16cv3-dBqDuVq0QTk5Pfz7ul7JH2lY7xcsgbYGzAl4gM/edit?gid=0#gid=0

### 23/09/2026
## Python Code Implementation

#### 1. Write a Python program which accepts a sequence of comma separated 4 digit binary numbers as its input and then check whether they are divisible by 5 or not. The numbers that are divisible by 5 are to be printed in a comma separated sequence.
#### Example: 0100,0011,1010,1001
#### Then the output should be: 1010

```
num = input().split()
for i in num:
    if int(i,2)%5==0:
        print(i)
```

#### 2. Write a Python program that accepts a sentence and calculate the number of letters and digits. 
#### Suppose the following input is supplied to the program: hello world! 123
#### Then, the output should be:
#### LETTERS 10
#### DIGITS 3

```
sentence = input()
letters=0
digit=0
for i in sentence:
    if i.isalpha():
        letters+=1
    elif i.isdigit():
        digit+=1
print("LETTER: ",letters)
print("DIGIT: ",digit)
```

#### 3. Write a program which can compute the factorial of a given numbers.The results should be printed in a comma-separated sequence on a single line.
#### Suppose the following input is supplied to the program:8
#### Then, the output should be: 40320

```
n = int(input())
fact=1
for i in range(1,n+1):
    fact*=i
print(fact)
```
