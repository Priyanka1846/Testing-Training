# HCL Automation Testing Training

## 17 September 2026

### Test Case Documentation

Created and documented test cases based on application requirements using a structured test case format.

#### Concepts Covered

- Test Case ID
- Test Case Description
- Preconditions
- Test Steps
- Test Data
- Expected Result
- Actual Result
- Test Status

**Task:** [Test Case Documentation](https://docs.google.com/spreadsheets/d/1RXd-QSDysk9iYf62sDZA2-BzGseUhxkbaIV3ppgLlEo/edit?gid=0#gid=0)

---

## 18 September 2026

### Test Case Using Jira

Created and managed test cases using Jira as part of the software testing workflow.

#### Concepts Covered

- Jira Issues
- Test Case Tracking
- Issue Identification
- Test Execution
- Status Tracking
- Defect Management

**Task:** [Jira Issue T1-22](https://priyankasworkspace-34516593.atlassian.net/browse/T1-22)

---

## 22 September 2026

### Equivalence Partition Test Case Exercises

Practiced designing test cases using the Equivalence Partitioning test design technique.

Equivalence Partitioning divides input data into different groups, or equivalence classes, where the system is expected to behave similarly for values within the same class.

#### Example

For an input field that accepts values from 1 to 100:

| Partition | Range | Classification |
|---|---|---|
| Partition 1 | Less than 1 | Invalid |
| Partition 2 | 1–100 | Valid |
| Partition 3 | Greater than 100 | Invalid |

**Task:** [Equivalence Partition Exercises](https://docs.google.com/spreadsheets/d/16cv3-dBqDuVq0QTk5Pfz7ul7JH2lY7xcsgbYGzAl4gM/edit?gid=0#gid=0)

---

## 23 September 2026

### Python Code Implementation

Implemented Python programs as part of the programming and automation testing training.

#### 1. Binary Numbers Divisible by 5

**Problem**

Write a Python program that accepts a sequence of comma-separated 4-digit binary numbers and checks whether they are divisible by 5. The numbers divisible by 5 should be printed.

**Example Input**

```text
0100,0011,1010,1001
```

**Expected Output**

```text
1010
```

**Implementation**

```python
num = input().split()

for i in num:
    if int(i, 2) % 5 == 0:
        print(i)
```
---

#### 2. Count Letters and Digits

**Problem**

Write a Python program that accepts a sentence and calculates the number of letters and digits.

**Example Input**

```text
hello world! 123
```

**Expected Output**

```text
LETTERS 10
DIGITS 3
```

**Implementation**

```python
sentence = input()

letters = 0
digit = 0

for i in sentence:
    if i.isalpha():
        letters += 1
    elif i.isdigit():
        digit += 1

print("LETTER: ", letters)
print("DIGIT: ", digit)
```
---

#### 3. Factorial of a Number

**Problem**

Write a Python program to calculate the factorial of a given number.

**Example Input**

```text
8
```

**Expected Output**

```text
40320
```

**Implementation**

```python
n = int(input())

fact = 1

for i in range(1, n + 1):
    fact *= i

print(fact)
```
---
## 24 September 2026

### Test Metrix

Created and documented the test matrix with requirements and test cases.

#### Metrics Covered
- Test Coverage
- Test Execution Percentage
- Pass Rate
- Fail Rate
- Total Defects
- Critical Defect Percentage
- Defect Distribution
- Mean Response Time
- Median Response Time

**Task:** [Test Metrics](https://docs.google.com/spreadsheets/d/1kFllSGDlt9accJvxfsRuHqLC3M2HJn2ZAn0iDP76MyY/edit?gid=0#gid=0)

---
